На абедзвюх віртуалках, каб працаваў цэнтос:

```
sed -i s/mirror.centos.org/vault.centos.org/g /etc/yum.repos.d/CentOS*.repo
sed -i s/^#.*baseurl=http/baseurl=http/g /etc/yum.repos.d/CentOS*.repo
sed -i s/^mirrorlist=http/#mirrorlist=http/g /etc/yum.repos.d/CentOS*.repo
```

Для яндэкса-шмяндэкса ў 4 лабе трэба браць версію не 7, а 7.0.1406

Пасля лухты, якую робяць з гіпервізарам-шміпершмізарам у канцы 4 лабы, каб потым далей рабіць лабы, трэба выканаць:
```
bcdedit /set hypervisorlaunchtype off
```
...і перазапусціць комп

...а пасля лабак, калі спатрэюіцца докер, напрыклад, які адваліцца, трэба выканаць:
```
bcdedit /set hypervisorlaunchtype auto
```
...і перазапусціць комп