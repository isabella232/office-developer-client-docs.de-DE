---
<<<<<<< HEAD-Titel: LineSeparator-Eigenschaft (ADO) TOCTitle: LineSeparator-Eigenschaft (ADO) === Titel: LineSeparator-Eigenschaft (ADO) TOCTitle: LineSeparator-Eigenschaft (ADO)
>>>>>>> Master Ms:assetid: 9f1323cd-d4ed-2bfa-554b-faebab529548 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249729(v=office.15) Ms:contentKeyID: 48546676 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="lineseparator-property-ado"></a>LineSeparator-Eigenschaft (ADO)
=======
# <a name="lineseparator-property-ado"></a>LineSeparator-Eigenschaft (ADO)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Gibt das binäre Zeichen an, das als Zeilentrennzeichen in [Stream](stream-object-ado.md)-Textobjekten verwendet wird.

<<<<<<< Kopf
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
=======
## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte
>>>>>>> master

Legt einen [LineSeparatorsEnum](lineseparatorsenum.md)-Wert fest, der das im **Stream** -Objekt verwendete Linientrennzeichen angibt, oder gibt diesen Wert zurück. Der Standardwert lautet **adCRLF**.

## <a name="remarks"></a>Hinweise

**LineSeparator** wird verwendet, um beim Lesen des Inhalts eines **Stream** -Textobjekts Zeilen zu interpretieren. Zeilen können mit der [SkipLine](skipline-method-ado.md)-Methode übersprungen werden.

**LineSeparator** wird nur bei **Stream**-Textobjekten verwendet ([Type](type-property-ado-stream.md) ist **adTypeText**). Diese Eigenschaft wird ignoriert, wenn **Type** auf **adTypeBinary** festgelegt ist.

