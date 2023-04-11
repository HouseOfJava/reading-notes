# Serverless Functions


Reading Questions

What are the key characteristics of serverless computing, and how does it differ from traditional server-based architectures?

Serverless computing comes prebuilt with functionality for users, also they differ by not requiring built in infastructure

How can one get started with Vercel, and what are the main steps involved in deploying a serverless function using Vercel?

One can sign up for vercel and link their prefered source code library. Once connected the user to enabled a repository to launch from vercel

What are APIs, and how can they be utilized in Python applications to access and manipulate data from external sources?

APIs are mechanisms that enable two software components to communicate with each other using a set of definitions and protocols.
In Python you can make calls to an APi to retrieve and manipulate data using built in dependencies.

What is the Requests library in Python, and how can it be used to interact with APIs by sending HTTP requests? Can you provide an example of a basic GET request using the Requests library?

The requests library is the de facto standard for making HTTP requests in Python. It abstracts the complexities of making requests behind a beautiful, simple API so that you can focus on interacting with services and consuming data in your application


```class handler(BaseHTTPRequestHandler):
    def do_GET(self):
        s = self.path
        url_components = parse.urlsplit(s)
        # print('url.components', url_components)
        query_string_list = parse.parse_qsl(url_components.query)
        # print("query.string.list", query_string_list)
        dic = dict(query_string_list)
        capital = dic.get('capital')
        country = dic.get('country')

        if capital:
            capital_url = f"https://restcountries.com/v3.1/capital/{capital}"
            r = requests.get(capital_url)
            data = r.json()
            definitions = []```
