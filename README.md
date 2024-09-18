# PyNetCat
A security tool for reading from and writing to network connections using TCP Protocol

# Usage
python3 pynetcat.py [-h] [-c] [-e EXECUTE] [-l] [-p PORT] [-t TARGET] [-u UPLOAD]

# Options
  -h, --help            show this help message and exit
  -c, --command         command shell
  -e EXECUTE, --execute EXECUTE
                        execute specified command
  -l, --listen          listen
  -p PORT, --port PORT  specified port
  -t TARGET, --target TARGET
                        specified IP
  -u UPLOAD, --upload UPLOAD
                        upload file

# Examples
pynetcat.py -t 192.168.1.108 -p 5555 -l -c # command shell
pynetcat.py -t 192.168.1.108 -p 5555 -l -u=mytest.txt # upload to file
pynetcat.py -t 192.168.1.108 -p 5555 -l -e="cat /etc/passwd" # execute command
echo 'ABC' | ./pynetcat.py -t 192.168.1.108 -p 135 # echo text to server port 135
pynetcat.py -t 192.168.1.108 -p 5555 # connect to server
