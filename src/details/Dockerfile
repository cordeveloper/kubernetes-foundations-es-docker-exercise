FROM ruby:3.3.0-slim

WORKDIR /opt/microservices

COPY Gemfile Gemfile.lock ./
COPY details.rb ./
RUN  bundle install

ARG service_version=v1
ARG enable_external_book_service=false

ENV SERVICE_VERSION=${service_version}
ENV ENABLE_EXTERNAL_BOOK_SERVICE=${enable_external_book_service}

EXPOSE 9080

RUN useradd -u 1000 myuser
USER myuser

CMD ["ruby", "details.rb", "9080"]
