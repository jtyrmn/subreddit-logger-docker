FROM mcr.microsoft.com/dotnet/sdk:7.0

RUN apt update && apt install git
WORKDIR /build

RUN git clone https://github.com/jtyrmn/subreddit-logger-portal .
RUN dotnet restore

RUN dotnet publish -c release -o /app


ENTRYPOINT [ "/app/subreddit-logger-portal" ]