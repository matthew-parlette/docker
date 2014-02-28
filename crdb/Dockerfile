FROM ubuntu
MAINTAINER matthew.parlette@gmail.com

# use the precise (12.04) repository
RUN echo "deb http://archive.ubuntu.com/ubuntu precise main universe" > /etc/apt/sources.list
RUN apt-get update
RUN apt-get install -q -y git ruby1.9.1 ruby1.9.1-dev build-essential libpq-dev libv8-dev libsqlite3-dev
RUN apt-get install -q -y nodejs

RUN gem install bundler

#create rails user with /rails home
#RUN adduser --disabled-password --home=/rails --gecos "" rails

#copy the app
ADD crdb /rails
#ADD production.sqlite /rails/db/production.sqlite
#RUN chown -R rails:rails /rails

#copy and execute setup script
ADD scripts/setup /setup
#RUN /setup

#copy the start script
ADD scripts/start /start

EXPOSE 3000
#USER rails
CMD /start

