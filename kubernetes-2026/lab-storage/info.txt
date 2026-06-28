• Zobacz domyślny StorageClass: kubectl get sc

• Stwórz PVC

• Napisz StatefulSet z volumeClaimTemplates

• kubectl exec do Poda — utwórz dane testowe

• Restart Poda i sprawdź że dane przeżyły

• PostgreSQL jako StatefulSet z PVC

• Manualny backup: pg_dump + kopia PVC do tar:
    - kubectl exec -n default database-0 -- pg_dumpall -U postgres > backup_all.sql.tar

• Manualny restore z backupu — udokumentuj procedurę
    - kubectl exec -n default database-0 -- pg_restore -U postgres -Fc -f backup.dump


Problemy:
- Problem z pull image PostgreSQL
- Problem z podłączeniem do bazy
- Nieprawidłowy tag przy obrazie
- Brak dodania w env użytkowanika