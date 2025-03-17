#!/bin/bash  
# Script de sauvegarde automatique des logs  

LOG_DIR="/var/log"  
BACKUP_DIR="/home/user/backup_logs"  
mkdir -p $BACKUP_DIR  

tar -czf $BACKUP_DIR/logs_$(date +%F).tar.gz $LOG_DIR  
echo "Sauvegarde terminée : $BACKUP_DIR/logs_$(date +%F).tar.gz"  
