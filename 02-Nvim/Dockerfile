# docker build -t snkkid/nvim .
# docker container run --name nvim -it --rm -v c/:/mnt/c snkkid/nvim
FROM alpine:latest
RUN apk add yarn git python3 cargo neovim ripgrep alpine-sdk bash gzip unzip py3-pip --update
RUN LV_BRANCH='release-1.3/neovim-0.9' su -c "bash <(curl -s https://raw.githubusercontent.com/lunarvim/lunarvim/release-1.3/neovim-0.9/utils/installer/install.sh) --no-install-dependencies"
RUN curl https://github.com/ryanoasis/nerd-fonts/blob/master/patched-fonts/RobotoMono/Regular/RobotoMonoNerdFont-Regular.ttf --create-dirs -o ~/.local/share/fonts/RobotoMonoNerdFont-Regular.ttf
ENV ENV=/root/.ashrc
RUN echo export PATH="$HOME/.local/bin:$PATH" >> /root/.ashrc
RUN echo "alias nvim=lvim" >> /root/.ashrc
#RUN echo -e $'\n\
#lvim.plugins =\n\
#{\n\
#  {\n\
#    "kwakzalver/duckytype.nvim",\n\
#    lazy = true,\n\
#    cmd = "DuckyType",\n\
#    config = function()\n\
#      require("duckytype").setup{}\n\
#    end,\n\
#  },\n\
#}' >> /root/.config/lvim/config.lua
RUN nvim +LvimUpdate +q
RUN nvim +:checkhealth +:qa!
