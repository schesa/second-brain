# IEC 62443


# Linux

#### **Variables**

```typeset -i (integer)```  
```declare -i (integer)```  
```declare -r (readonly constant)```

#### **Arrays**

```typeset -a foo=(a b c)```  
```typeset -A associative-array (dict)```

```echo $foo```  
\# a  
```echo ${foo[@]}```  
\# a b c  
```echo $foo[@]```  
\# a[@]  
```echo ${#foo}```  
\# 3

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
```systemctl start NetworkManager``` - start/stop/restart  
```systemctl is-active NetworkManager```

##### Enabled - service is configured to start at system boot time  
```systemctl enable NetworkManager``` - disable  
```systemctl is-enabled NetworkManager```

