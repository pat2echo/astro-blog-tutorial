# Install on Bare Metal Linux

1. Install nvm and node  

- Supported node versions v18.17.1 or v20.3.0 or later. (v19 is not supported.)

- Check if you have node
```
node -v
```

- Check if you have nvm
```
nvm --version
```

- Install nvm and node
```
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash source ~/.bashrc

nvm install node
```

- Set default node version
```
nvm alias default node
```

## reference
https://docs.astro.build/en/tutorial/1-setup/1/