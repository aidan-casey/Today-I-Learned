# List all members of a Group

## To list members of a group

```bash
grep '{{groupName}}' /etc/group
```

## To add some color

```bash
grep -i --color '{{groupName}}' /etc/group
```

## To list only member names of a group

```bash
awk -F':' '/{{groupName}}/{print $4}' /etc/group
```

[Found on CyberCiti](https://www.cyberciti.biz/faq/linux-list-all-members-of-a-group/)