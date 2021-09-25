---
title: ActiveConnection-Eigenschaft (ADO)
TOCTitle: ActiveConnection property (ADO)
ms:assetid: 5501b2d7-b62c-5fff-1edd-2b7efb3f8c4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249281(v=office.15)
ms:contentKeyID: 48544918
ms.date: 10/17/2018
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231115
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 3be71b700b670309a021de491c9e2af2e448084d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59586271"
---
# <a name="activeconnection-property-ado"></a>ActiveConnection-Eigenschaft (ADO)

**Gilt für**: Access 2013, Office 2013

Gibt an, zu welchem [Connection](connection-object-ado.md)-Objekt das angegebene [Command](command-object-ado.md)-, [Recordset](recordset-object-ado.md)- oder [Record](record-object-ado.md)-Objekt derzeit gehört.

## <a name="settings-and-return-values"></a>Einstellungen- und Rückgabewerte

Mit dieser Eigenschaft wird ein Wert vom Datentyp **String** zurückgegeben oder festgelegt, der eine Definition für eine Verbindung enthält, falls die Verbindung geschlossen ist, oder ein Wert vom Datentyp **Variant**, der das aktuelle **Connection**-Objekt enthält, falls die Verbindung geöffnet ist. Der Standard ist ein nullwertiger Objektverweis. Siehe [ConnectionString](connectionstring-property-ado.md)-Eigenschaft.

## <a name="remarks"></a>HinwBemerkungeneise

Bestimmen Sie mithilfe der **ActiveConnection**-Eigenschaft das **Connection**-Objekt, über das das angegebene **Command**-Objekt ausgeführt oder das angegebene **Recordset**-Objekt geöffnet wird.

### <a name="command"></a>Befehl

Für **Command**-Objekte weist die **ActiveConnection**-Eigenschaft Lese-/Schreibzugriff auf.

Ein Fehler wird erzeugt, wenn Sie die [Execute](/office/vba/access/concepts/miscellaneous/execute-method-ado-command.md)-Methode für ein **Command**-Objekt aufrufen, bevor Sie diese Eigenschaft auf ein geöffnetes **Connection**-Objekt oder eine gültige Verbindungszeichenfolge festgelegt haben.

**Microsoft Visual Basic:** Durch Festlegen der **ActiveConnection-Eigenschaft** auf *Nothing* wird das **Command-Objekt** von der aktuellen **Verbindung** getrennt und bewirkt, dass der Anbieter alle zugeordneten Ressourcen in der Datenquelle freigibt. Sie können dann das **Command**-Objekt demselben oder einem anderen **Connection**-Objekt zuordnen. Einige Anbieter ermöglichen es, die Einstellung der Eigenschaft zwischen zwei **Connection**-Objekten zu ändern, ohne dass Sie die Eigenschaft zuerst auf *Nothing* festlegen müssen.

Wenn die [Parameters](parameters-collection-ado.md)-Auflistung des **Command**-Objekts vom Anbieter bereitgestellte Parameter enthält, wird die Auflistung gelöscht, falls Sie die **ActiveConnection**-Eigenschaft auf *Nothing* oder auf ein anderes **Connection**-Objekt festlegen. Wenn Sie [Parameter](parameter-object-ado.md)-Objekte manuell erstellen und zum Füllen der **Parameters**-Auflistung des **Command**-Objekts verwenden, bleibt durch Festlegen der **ActiveConnection**-Eigenschaft auf *Nothing* oder auf ein anderes **Connection**-Objekt die **Parameters**-Auflistung unverändert.

Durch Schließen des **Connection**-Objekts, dem ein **Command**-Objekt zugeordnet ist, wird die **ActiveConnection**-Eigenschaft auf *Nothing* festgelegt. Ein Fehler wird generiert, wenn Sie diese Eigenschaft auf ein geschlossenes **Connection**-Objekt festlegen.

### <a name="recordset"></a>Recordset

Für geöffnete **Recordset**-Objekte oder für **Recordset**-Objekte, deren [Source](source-property-ado-recordset.md)-Eigenschaft auf ein gültiges **Command**-Objekt festgelegt ist, ist die **ActiveConnection**-Eigenschaft schreibgeschützt. Andernfalls weist sie Lese-/Schreibzugriff auf.

Sie können für diese Eigenschaft ein gültiges **Connection** -Objekt oder eine gültige Verbindungszeichenfolge festlegen. In diesem Fall erstellt der Anbieter mithilfe dieser Definition ein neues **Connection** -Objekt und öffnet die Verbindung. Darüber hinaus kann der Anbieter diese Eigenschaft auf ein neues **Connection** -Objekt festlegen, um Ihnen eine Möglichkeit für den Zugriff auf das **Connection** -Objekt zu bieten, damit Sie erweiterte Fehlerinformationen abrufen oder andere Befehle ausführen können.

Wenn Sie das Argument *ActiveConnection* der [Open](open-method-ado-recordset.md)-Methode zum Öffnen eines **Recordset**-Objekts verwenden, erbt die **ActiveConnection**-Eigenschaft den Wert des Arguments.

Wenn Sie die **Source**-Eigenschaft des **Recordset**-Objekts auf eine gültige **Command**-Objektvariable festlegen, erbt die **ActiveConnection**-Eigenschaft des **Recordset**-Objekts die Einstellung der **ActiveConnection**-Eigenschaft des **Command**-Objekts.

**Remote Data Service Usage:** When used on a client-side Recordset object, this property can be set only to a connection string or (in Microsoft Visual Basic or Visual Basic, Scripting Edition) to *Nothing*.

### <a name="record"></a>Aufzeichnen

Diese Eigenschaft weist Lese-/Schreibzugriff auf, wenn das **Record**-Objekt geschlossen ist, und kann eine Verbindungszeichenfolge oder einen Verweis auf ein geöffnetes **Connection**-Objekt enthalten. Diese Eigenschaft ist schreibgeschützt, wenn das **Record**-Objekt geöffnet ist, und enthält einen Verweis auf ein geöffnetes **Connection**-Objekt.

Ein **Connection**-Objekt wird implizit erstellt, wenn das **Record**-Objekt über eine URL geöffnet wird. Öffnen Sie das **Record**-Objekt mit einem vorhandenen, geöffneten **Connection**-Objekt, indem Sie dem **Connection**-Objekt diese Eigenschaft zuweisen, oder mithilfe des **Connection**-Objekts als Parameter im Aufruf der [Open](open-method-ado-record.md)-Methode. Wenn der **Datensatz** aus einem vorhandenen **Record-** oder [Recordset-Objekt](recordset-object-ado.md)geöffnet wird, wird er automatisch dem **Connection-Objekt** dieses **Record-** oder **Recordset-Objekts** zugeordnet.

> [!NOTE]
> Bei URLs, die das HTTP-Schema verwenden, wird automatisch der [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) aufgerufen. Weitere Informationen finden Sie unter [Absolute und relative URLs.](absolute-and-relative-urls.md)
