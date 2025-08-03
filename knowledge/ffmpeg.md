### gifの綺麗な出力方法
`ffmpeg -i input.mp4 -vf "fps=30,scale=1920:1080:flags=lanczos" output.gif
`