---
<<<<<<< HEAD-Titel: CommandType-Eigenschaft (ADO) TOCTitle: CommandType-Eigenschaft (ADO) === Titel: CommandType-Eigenschaft (ADO) TOCTitle: CommandType-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: c8d4fc1c-502b-11f3-af9d-605a03b6f056 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249976(v=office.15) Ms:contentKeyID: 48547663 ms.date: 09/18/2015 Mtps_version: Office. 15 f1_keywords:
- ado210.chm1231125 f1_categories:
- Office.Version=v15
---

<<<<<<< HEAD
# <a name="commandtype-property-ado"></a>CommandType-Eigenschaft (ADO)
=======
# <a name="commandtype-property-ado"></a>CommandType-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt den Typ eines [Command](command-object-ado.md)-Objekts an.

<<<<<<< HEAD
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
>>>>>>> master

Mit dieser Eigenschaft wird mindestens ein [CommandTypeEnum](commandtypeenum.md)-Wert festgelegt oder zurückgegeben.

> [!NOTE]
> [!HINWEIS] Verwenden Sie die **CommandTypeEnum** -Werte von **adCmdFile** oder **adCmdTableDirect** nicht zusammen mit **CommandType**. Diese Werte können nur als Optionen für die Methoden [Open](open-method-ado-recordset.md) und [Requery](requery-method-ado.md) eines [Recordset](recordset-object-ado.md)-Objekts verwendet werden.


## <a name="remarks"></a>Hinweise

Verwenden Sie die **CommandType** -Eigenschaft zum Optimieren der Evaluierung der [CommandText](commandtext-property-ado.md)-Eigenschaft.

<<<<<<< HEAD, wenn der Wert der **CommandType** -Eigenschaft gleich **AdCmdUnknown** (Standardwert), treten möglicherweise Leistung beeinträchtigt, da ADO Aufrufe an den Anbieter, um festzustellen, ob erfolgen muss die **CommandText** -Eigenschaft ist eine SQL-Anweisung, eine gespeicherte Prozedur oder einen Tabellennamen. Wenn Sie, die Sie verwenden die **CommandType** -Eigenschaft festlegen wissen, die welche Art des Befehls, weist ADO fahren Sie direkt mit der relevante Code. Wenn die **CommandType** -Eigenschaft den Typ des Befehls in der **CommandText** -Eigenschaft nicht übereinstimmt, tritt ein Fehler beim Aufrufen der [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\)) -Methode.
===, Wenn der Wert der **CommandType** -Eigenschaft **AdCmdUnknown** (Standardwert) ist, treten möglicherweise Leistung beeinträchtigt, da ADO Aufrufe an den Anbieter treffen muss zu ermitteln, ob die **CommandText** -Eigenschaft eine SQL-Anweisung ist ein gespeicherte Prozedur oder einen Tabellennamen. Wenn Sie, die Sie verwenden die **CommandType** -Eigenschaft festlegen wissen, die welche Art des Befehls, weist ADO fahren Sie direkt mit der relevante Code. Wenn die **CommandType** -Eigenschaft den Typ des Befehls in der **CommandText** -Eigenschaft nicht übereinstimmt, tritt ein Fehler beim Aufrufen der [Execute](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command) -Methode.
>>>>>>> master

