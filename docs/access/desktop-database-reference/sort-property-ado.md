---
<<<<<<< HEAD-Titel: Sort-Eigenschaft (ADO) TOCTitle: Sort-Eigenschaft (ADO) === Titel: Sortieren-Eigenschaft (ADO) TOCTitle: Sortieren-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: f2a39b7f-8b96-cd1a-8248-71f8b867454a Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250230(v=office.15) Ms:contentKeyID: 48548652 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="sort-property-ado"></a>Sort-Eigenschaft (ADO)
=======
# <a name="sort-property-ado"></a>Sort-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt einen oder mehrere Feldnamen an, nach denen das [Recordset](recordset-object-ado.md) sortiert wird, und gibt an, ob die einzelnen Felder aufsteigend oder absteigend sortiert werden.

<<<<<<< Kopf
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
>>>>>>> master

Legt einen **String** -Wert fest, der die Feldnamen im **Recordset** -Objekt angibt, nach denen sortiert wird, oder gibt den Wert zurück. Jeder Name wird durch ein Komma getrennt, ggf. gefolgt von einer Leerstelle und dem Schlüsselwort. **ASC** sortiert das Feld in aufsteigender, **DESC** in absteigender Reihenfolge. Wenn Sie kein Schlüsselwort angeben, wird das Feld standardmäßig in aufsteigender Reihenfolge sortiert.

## <a name="remarks"></a>Hinweise

Für diese Eigenschaft muss die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft auf **adUseClient** festgelegt sein. Ein temporärer Index wird für jedes Feld erstellt, das in der **Sort** -Eigenschaft angegeben ist, sofern noch kein Index vorhanden ist.

Der Sortiervorgang ist effizient, da Daten nicht physisch neu angeordnet werden, sondern einfach nur in der im Index angegebenen Reihenfolge auf die Daten zugegriffen wird.

Wenn Sie für die **Sort** -Eigenschaft eine leere Zeichenfolge festlegen, werden die Zeilen in die ursprüngliche Reihenfolge zurückgesetzt und temporäre Indizes gelöscht. Vorhandene Indizes werden nicht gelöscht.

Angenommen Sie, ein **Recordset-Objekt** namens *FirstName*, *LastName*und *MiddleInitial*drei Felder enthält. Legen Sie die **Sort** -Eigenschaft auf die Zeichenfolge "LastName DESC, FirstName ASC" die Reihenfolge der **Recordset-Objekt** nach dem Nachnamen in absteigender Reihenfolge und dann nach dem Vornamen in aufsteigender Reihenfolge. Der Mittelname wird ignoriert.

Felder können nicht "ASC" oder "DESC" benannt werden, da sonst ein Konflikt mit den Schlüsselwörtern **ASC** und **DESC** auftritt. Geben Sie einem Feld mit einem Konflikte verursachenden Namen einen Alias. Verwenden Sie dazu das Schlüsselwort **AS** in der Abfrage, die das **Recordset** -Objekt zurückgibt.

