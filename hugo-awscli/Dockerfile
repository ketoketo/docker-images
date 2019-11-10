FROM golang:1.12.1

WORKDIR /work
RUN curl -O https://bootstrap.pypa.io/get-pip.py \
  && python get-pip.py \
  && pip install awscli \
  && pip install --upgrade awscli \
  && mkdir $HOME/src \
  && cd $HOME/src \
  && git clone https://github.com/gohugoio/hugo.git \
  && cd hugo \
  && go install \
  && ln -sf /usr/share/zoneinfo/Asia/Tokyo /etc/localtime

WORKDIR $GOPATH
