---
<<<<<<< HEAD-Titel: CacheSize-Eigenschaft (ADO) TOCTitle: CacheSize-Eigenschaft (ADO) === Titel: CacheSize-Eigenschaft (ADO) TOCTitle: CacheSize-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: 42f86cc0-30dc-669b-9e65-5e7ecd52c4d7 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249200(v=office.15) Ms:contentKeyID: 48544491 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< HEAD
# <a name="cachesize-property-ado"></a>CacheSize-Eigenschaft (ADO)
=======
# <a name="cachesize-property-ado"></a>CacheSize-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt die Anzahl von Datensätzen aus einem [Recordset](recordset-object-ado.md)-Objekt an, die lokal im Arbeitsspeicher zwischengespeichert werden.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
>>>>>>> master

Mit dieser Eigenschaft wird ein Wert vom Datentyp Long festgelegt oder zurückgegeben, der größer als 0 sein muss. Der Standard ist 1.

## <a name="remarks"></a>Hinweise

Verwenden Sie die **CacheSize** -Eigenschaft, um zu steuern, wie viele Datensätze gleichzeitig vom Anbieter in den lokalen Arbeitsspeicher abgerufen werden. Wenn z. B. **CacheSize** den Wert 10 hat, ruft der Anbieter, nachdem er zunächst das **Recordset** -Objekt geöffnet hat, die ersten 10 Datensätze in den lokalen Arbeitsspeicher ab. Beim Durchlaufen des **Recordset** -Objekts gibt der Anbieter die Daten aus dem lokalen Arbeitsspeicherpuffer zurück. Sobald Sie hinter den letzten Datensatz im Cache gelangt sind, ruft der Anbieter die nächsten 10 Datensätze von der Datenquelle in den Cache ab.

> [!NOTE]
> [!HINWEIS] **CacheSize** basiert auf der anbieterspezifischen Eigenschaft **Maximale Anzahl geöffneter Zeilen** (in der **Properties** -Auflistung des **Recordset** -Objekts). **CacheSize** kann nicht auf einen höheren Wert als **Maximale Anzahl geöffneter Zeilen** festgelegt werden. Legen Sie **Maximale Anzahl geöffneter Zeilen** fest, um die Anzahl von Zeilen zu ändern, die vom Anbieter geöffnet werden können.

Der Wert von **CacheSize** kann während des Lebenszyklus des **Recordset** -Objekts angepasst werden, aber die Änderung dieses Werts wirkt sich nur auf die Anzahl von Datensätzen im Cache nach nachfolgendem Abrufen von der Datenquelle aus. Durch das Ändern des Eigenschaftswerts allein werden die aktuellen Inhalte des Caches nicht geändert.

Wenn weniger Datensätze abzurufen sind, als durch **CacheSize** angegeben sind, gibt der Anbieter die restlichen Datensätze zurück, und es tritt kein Fehler auf.

Die Einstellung 0 für **CacheSize** ist nicht zulässig. In diesem Fall würde ein Fehler gemeldet.

Aus dem Cache abgerufene Datensätze enthalten keine Änderungen, die andere Benutzer gleichzeitig an den Quelldaten vorgenommen haben. Verwenden Sie die [Resync](resync-method-ado.md)-Methode, um eine Aktualisierung aller zwischengespeicherter Daten zu erzwingen.

Wenn CacheSize auf einen Wert größer 1 festgelegt wird, können die Navigationsmethoden (Move, MoveFirst, MoveLast, MoveNext und MovePrevious) dazu führen, dass zu einem gelöschten Datensatz navigiert wird, falls der Löschvorgang nach dem Abrufen der Datensätze erfolgt. Nach dem Abrufen werden nachfolgende Löschvorgänge erst im Datencache übernommen, wenn Sie versuchen, auf einen Datenwert in einer gelöschten Zeile zuzugreifen. Wenn Sie allerdings CacheSize auf 1 festlegen, wird dieses Problem beseitigt, weil gelöschte Zeilen nicht abgerufen werden können.

