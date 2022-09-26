```bash
# Merge multiple images to one video
ffmpeg -framerate 30 -pattern_type glob -i "*.png" -pix_fmt yuv420p -c:v libx264 "OUTPUT_FILE"

# Resize image but keep the aspect ratio
ffmpeg -i "INPUT_FILE" -vf scale="360:-1" "OUTPUT_FILE"

# Resize based on input width iw and input height ih
ffmpeg -i "INPUT_FILE" -vf scale="iw/2:ih/2" "OUTPUT_FILE"

# Combine multiple images into one (three singles into one row of three)
ffmpeg -i "IMAGE_1" -i "IMAGE_2" -i "IMAGE_3" -filter_complex "[0][2][1]hstack=inputs=3" "OUTPUT_IMAGE"

# Expand image by adding colored padding
convert "UNPADDED_IMAGE" -background "#ECE7DD" -gravity center -extent 7200x4000 "PADDED_IMAGE"

# Crop video, centered
ffmpeg -i "INPUT_VIDEO" -filter:v "crop=in_w-30:in_h-18" -c:a copy "OUTPUT_VIDEO"

# Convert Quicktime screen recording to gif
ffmpeg -i "SCREEN_RECORDING.MOV" -pix_fmt rgb24 -r 20 -s 400x400 "OUTPUT.GIF"

# Apply multiple filters: invert colors, flip horizontally and convert to greyscale
ffmpeg -i "INPUT_FILE" -vf lutrgb="r=negval:g=negval:b=negval,hflip,hue=s=0" "OUTPUT_FILE"
```
