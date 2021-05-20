FROM debian:latest

WORKDIR /app
RUN mkdir -p /app

RUN apt update
RUN apt install -y vim git jq curl procps ssh

RUN adduser --gecos "cloud training" --disabled-password app
RUN chown -R app:app /app
RUN sed -e 's/^"au BufReadPost/au BufReadPost/' -i /etc/vim/vimrc
RUN echo "set number\nsyntax on\nset shiftwidth=2" > /home/app/.vimrc

USER app
RUN ssh-keygen -t rsa -q -f /home/app/.ssh/id_rsa

