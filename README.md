from pytube import YouTube
# from sys import argv


links = input("enter the link:-")
yt = YouTube(links)

print("title: ",yt.title)
print("views: ",yt.views)
get_format = input("enter the format")
print("for audio enter ad")
if get_format== "ad" or get_format== "A":
    yd = yt.streams.get_audio_only()
    print("downloading please wait....")
    yd.download("/home/karnav/Downloads/")
    print("done...")
elif get_format=="v" or get_format== "V":
    yd = yt.streams.get_highest_resolution()
    print("downloading please wait....")
    yd.download("/home/karnav/Downloads/")
    print("done...")
