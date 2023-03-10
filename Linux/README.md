# Linux

#### **Variables**

```shell
$   typeset -i arg1=1 arg2=2 # integer    
$   declare -i arg1=1 arg2=2 # integer  
$   declare -r const="FILE" # readonly constant
```

#### **Arrays**

```shell
$   typeset -a foo=(a b c)  
$   declare -A assArray=( [A]=2 [B]=3 ) # associative-array (dict)  
$
$   echo $foo  
a 
$   echo ${foo[@]}  
a b c  
$   echo $foo[@]  
a[@]  
$   echo ${#foo}  
3
```

```${#VAR}``` - calculates the length of value $VAR or array length

#### **Brace expansion**

ex. ```echo {f..a}; echo {2,6,9}```  
```${}```

#### **Parameter expansion**

```${var^^}``` - all uppercase  
```${var:-$default}``` - default if var is unset   


#### **Command substitution**

```$()``` or ``` \`...\` ```  
ex. ```echo "hello $( s=world; echo "$s" )"```  
```$()``` is preffered - modern, can use nested commands, backtiks are considered "deprecated"  
Read command also uses a subshell for execution

#### **Systemd**

##### Active - service is running
```shell
$   systemctl start NetworkManager  # start/stop/restart  
$   systemctl is-active NetworkManager
```

##### Enabled - service is configured to start at system boot time  
```shell  
$   systemctl enable NetworkManager   # disable    
$   systemctl is-enabled NetworkManager
```


#### **HereDoc**  
For multiline appending. Works also with ssh

```shell
cat << EOF >> file.txt
The current working directory is: $PWD
You are logged in as: $(whoami)
EOF
```
