FROM dart:stable

WORKDIR /api-app

COPY pubspec.* ./
RUN dart pub get --no-precompile 
ADD . /api-app/

RUN dart pub get --offline --no-precompile 

COPY . . 
 
EXPOSE 7777

ENTRYPOINT [ "dart", "run", "conduit:conduit", "serve", "--port", "7777" ]