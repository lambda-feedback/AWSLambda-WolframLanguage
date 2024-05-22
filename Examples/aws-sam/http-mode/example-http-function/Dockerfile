FROM wolframresearch/aws-lambda-wolframlanguage:latest

COPY *.wl /var/task/

USER root

RUN cp -f /usr/local/Wolfram/WolframEngine/13.0/SystemFiles/Libraries/Linux-x86-64/libiomp5.so \
    /usr/local/Wolfram/WolframEngine/13.3/SystemFiles/Libraries/Linux-x86-64/libiomp5.so

COPY runtime-entrypoint.sh /runtime-entrypoint.sh

RUN chmod a+rx /runtime-entrypoint.sh

USER wolframengine

# Selected handler can be overridden by providing a different command in the template directly.
CMD ["http-handler-file"]