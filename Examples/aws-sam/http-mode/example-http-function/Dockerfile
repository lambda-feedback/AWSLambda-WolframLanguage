FROM wolframresearch/aws-lambda-wolframlanguage:latest

COPY *.wl /var/task/

RUN cp /usr/local/Wolfram/WolframEngine/13.0/SystemFiles/Libraries/Linux-x86-64/libiomp5.so \
    /usr/local/Wolfram/WolframEngine/13.3/SystemFiles/Libraries/Linux-x86-64/libiomp5.so

# Selected handler can be overridden by providing a different command in the template directly.
CMD ["http-handler-file"]