# python

- mac

        brew install python3
        
        /usr/local/bin/python3
        /usr/local/bin/pip3

- centos7

        yum -y install zlib-devel bzip2-devel openssl-devel ncurses-devel sqlite-devel readline-devel tk-devel gdbm-devel db4-devel libpcap-devel xz-devel
        cd /opt
        wget http://npm.taobao.org/mirrors/python/3.7.9/Python-3.7.9.tgz
        tar -xzf Python-3.7.9.tgz
        cd Python-3.7.9
        ./configure --prefix=/opt/python
        make && make install

        cat << EOF >> /etc/profile
        # python
        export PYTHON=/opt/python/bin
        export PATH=\$PATH:\$PYTHON
        EOF

        source /etc/profile
        pip3 install --upgrade pip
        
- win7 32

        https://www.python.org/ftp/python/3.7.6/python-3.7.6.exe

- source

        sudo -i
        yum install gcc openssl-devel bzip2-devel
        wget https://www.python.org/ftp/python/3.7.2/Python-3.7.2.tgz
        tar xzf Python-3.7.2.tgz
        cd Python-3.7.2
        ./configure
        make altinstall
        cd /usr/bin && ln -s /usr/local/bin/python3.7 python3
        python3 --version

        - if python=python3, fix yum
        sudo -i
        vi /usr/bin/yum -> #!/usr/bin/python2.7

        or

        which python -> e.g. /bin/python
        cd /bin/python && rm python
        ln -s /usr/bin/python2.7 python

        - install pip3
        sudo -i
        curl https://bootstrap.pypa.io/get-pip.py | python
        cd /usr/bin && ln -s /usr/local/bin/pip3 pip3

- pip3 install numpy

        import numpy as np
        X = np.array([[1,2]])
        X.shape
        W = np.array([[1,3,5],[2,4,6]])
        print(W)
        W.shape
        Y = np.dot(X, W)
        print(Y)

- pip3 install matplotlib
