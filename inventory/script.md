1. echo "[all]" > inventory

2. aws ec2 describe-instances \
   --query 'Reservations[*].Instances[*].PublicIpAddress' \
   --filters "Name=,Values=" \
   --output text >> inventory