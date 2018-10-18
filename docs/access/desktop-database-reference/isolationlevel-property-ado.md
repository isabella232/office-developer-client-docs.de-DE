---
<<<<<<< HEAD-Titel: IsolationLevel-Eigenschaft (ADO) TOCTitle: IsolationLevel-Eigenschaft (ADO) === Titel: IsolationLevel-Eigenschaft (ADO) TOCTitle: IsolationLevel-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: 19461be5-c94b-4b61-ce08-7abdf702c3dc Ms:mtpsurl: https://msdn.microsoft.com/library/JJ248939(v=office.15) Ms:contentKeyID: 48543493 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="isolationlevel-property-ado"></a>IsolationLevel-Eigenschaft (ADO)
=======
# <a name="isolationlevel-property-ado"></a>IsolationLevel-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt die Isolationsstufe für ein [Connection](connection-object-ado.md)-Objekt an.

<<<<<<< Kopf
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
>>>>>>> master

Legt einen [IsolationLevelEnum](isolationlevelenum.md)-Wert fest oder gibt den Wert zurück. Der Standardwert ist **AdXactChaos**.

## <a name="remarks"></a>Hinweise

Legen Sie mit der **IsolationLevel** -Eigenschaft die Isolationsstufe eines **Connection** -Objekts fest. Die Einstellung wird erst beim nächsten Aufrufen der [BeginTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Methode wirksam. Wenn die von Ihnen angeforderte Isolationsstufe nicht verfügbar ist, gibt der Anbieter möglicherweise die nächsthöhere Isolationsstufe zurück.

Die **IsolationLevel** -Eigenschaft ist nicht schreibgeschützt.

**Remote Data Service-Verwendung** Wenn für ein clientseitiges Connection-Objekt verwendet wird, kann die **IsolationLevel** -Eigenschaft nur auf **AdXactUnspecified**festgelegt werden.

Da Benutzer mit nicht verbundenen **Recordset** -Objekten in einem clientbasierten Cache arbeiten, können Probleme mit mehreren Benutzern auftreten. Wenn beispielsweise zwei unterschiedliche Benutzer versuchen, denselben Datensatz zu aktualisieren, hat der Benutzer Erfolg, der den Datensatz zuerst aktualisiert. Die Aktualisierungsanforderung des zweiten Benutzers verursacht einen Fehler.

