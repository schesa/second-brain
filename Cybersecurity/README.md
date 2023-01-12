# IEC 62443


# Linux

#### **Variables**

typeset -i (integer)

declare -i (integer)

declare -r (readonly constant)

#### **Arrays**

typeset -a foo=(a b c)

typeset -A associative-array (dict)

echo $foo
\# a
echo ${foo[@]}
\# a b c
echo $foo[@]
\# a[@]

${#VAR} - calculates the length of value $VAR

#### **Brace expansion**

ex. echo {f..a}; echo {2,6,9}

${}

#### **Command substitution**

$() or \`...\` 

ex. echo "hello $( s=world; echo "$s" )"

$() is preffered - modern, can use nested commands, backtiks are considered "deprecated"

Read command also uses a subshell for execution
