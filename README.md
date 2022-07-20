# Python-Chatroom
Source: https://dev.to/zeyu2001/build-a-chatroom-app-with-python-44fa

<h1>Broadcasting</h1>
<h2> The server tell all the client that he recieve new connection</h2>
class Server(threading.Thread):

    ...

    def run(self):

        ...

    def broadcast(self, message, source):

        for connection in self.connections:

#           Send to all connected clients except the source client
            if connection.sockname != source:
                connection.send(message)

---