```ruby
def create_printing_log
# return unless params[:daily_schedule][:detail_daily_schedules_attributes]
# return unless params[:daily_schedule][:detail_daily_schedules_attributes][:detail_daily_schedule_tasks_attributes]

task_attributes = params.dig(
	:daily_schedule,
	:detail_daily_schedules_attributes,
	0,
	:detail_daily_schedule_tasks_attributes
)

return unless task_attributes.is_a?(Hash) && task_attributes[:id].present?

detail_task = DetailDailyScheduleTask.find_by(id: task_attributes[:id])
return unless detail_task&.approval_status&.value&.>= DetailDailyScheduleTask.approval_status.applying.value

FScreenDetailDailyScheduleTaskPrintingLog.create!(
	detail_daily_schedule_task_id: detail_task.id,
	user_id: current_user.id,
	user_assign_type: load_office_role&.assign&.class&.to_s,
	user_assign_id: load_office_role&.assign&.id,
	created_at: Time.zone.now
)
end
```

