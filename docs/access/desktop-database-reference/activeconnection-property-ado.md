---
title: ActiveConnection-Eigenschaft (ADO)
TOCTitle: ActiveConnection Property (ADO)
ms:assetid: 5501b2d7-b62c-5fff-1edd-2b7efb3f8c4a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249281(v=office.15)
ms:contentKeyID: 48544918
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- ado210.chm1231115
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d44a17d192abdb68755a2010184b4fb4d6531174
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25476074"
---
# <a name="activeconnection-property-ado"></a>ActiveConnection-Eigenschaft (ADO)


**Betrifft**: Access 2013 | Office 2013

Gibt an, zu welchem [Connection](connection-object-ado.md)-Objekt das angegebene [Command](command-object-ado.md)-, [Recordset](recordset-object-ado.md)- oder [Record](record-object-ado.md)-Objekt derzeit gehört.

## <a name="settings-and-return-values"></a>Einstellungen und Rückgabewerte

Mit dieser Eigenschaft wird ein Wert vom Datentyp **String** zurückgegeben oder festgelegt, der eine Definition für eine Verbindung enthält, falls die Verbindung geschlossen ist, oder ein Wert vom Datentyp **Variant**, der das aktuelle **Connection** -Objekt enthält, falls die Verbindung geöffnet ist. Der Standard ist ein nullwertiger Objektverweis. Siehe [ConnectionString](connectionstring-property-ado.md)-Eigenschaft.

## <a name="remarks"></a>Hinweise

Bestimmen Sie mithilfe der **ActiveConnection** -Eigenschaft das **Connection** -Objekt, über das das angegebene **Command** -Objekt ausgeführt oder das angegebene **Recordset** -Objekt geöffnet wird.

**Command**

Für **Command** -Objekte weist die **ActiveConnection** -Eigenschaft Lese-/Schreibzugriff auf.

Ein Fehler wird erzeugt, wenn Sie die [Execute](https://msdn.microsoft.com/library/jj248785\(v=office.15\))-Methode für ein **Command** -Objekt aufrufen, bevor Sie diese Eigenschaft auf ein geöffnetes **Connection** -Objekt oder eine gültige Verbindungszeichenfolge festgelegt haben.

**Microsoft Visual Basic** Festlegen der **ActiveConnection** -Eigenschaft auf *Nothing* das **Command** -Objekt aus der aktuellen **Verbindung** trennt und bewirkt, dass den Anbieter keine zugeordneten Ressourcen für die Datenquelle freigeben. Sie können dann das **Command** -Objekt demselben oder einem anderen **Connection** -Objekt zuordnen. Einige Anbieter können Sie die Einstellung der Eigenschaft aus eine **Verbindung** zu einem anderen zu ändern, ohne dass zuerst die-Eigenschaft auf *Nothing*festgelegt.

Wenn die [Parameters](parameters-collection-ado.md) -Auflistung des **Command** -Objekts vom Anbieter bereitgestellte Parameter enthält, wird die Auflistung gelöscht, wenn Sie die **ActiveConnection** -Eigenschaft auf *Nothing* oder zu einer anderen **Connection** -Objekt festgelegt. Wenn Sie manuell [Parameter](parameter-object-ado.md) -Objekte erstellen und diese zum Füllen der **Parameters** -Auflistung des **Command** -Objekts verwenden, bewirkt, dass durch Festlegen der **ActiveConnection** -Eigenschaft auf *Nothing* oder zu einer anderen **Connection** -Objekt die **Parameters** -Auflistung erhalten bleibt.

Durch Schließen des **Connection**-Objekts, dem ein **Command**-Objekt zugeordnet ist, wird die **ActiveConnection**-Eigenschaft auf *Nothing* festgelegt. Ein Fehler wird generiert, wenn Sie diese Eigenschaft auf ein geschlossenes **Connection**-Objekt festlegen.

**Recordset**

Für geöffnete **Recordset** -Objekte oder für **Recordset** -Objekte, deren [Source](source-property-ado-recordset.md)-Eigenschaft auf ein gültiges **Command** -Objekt festgelegt ist, ist die **ActiveConnection** -Eigenschaft schreibgeschützt. Andernfalls weist sie Lese-/Schreibzugriff auf.

Sie können für diese Eigenschaft ein gültiges **Connection** -Objekt oder eine gültige Verbindungszeichenfolge festlegen. In diesem Fall erstellt der Anbieter mithilfe dieser Definition ein neues **Connection** -Objekt und öffnet die Verbindung. Darüber hinaus kann der Anbieter diese Eigenschaft auf ein neues **Connection** -Objekt festlegen, um Ihnen eine Möglichkeit für den Zugriff auf das **Connection** -Objekt zu bieten, damit Sie erweiterte Fehlerinformationen abrufen oder andere Befehle ausführen können.

Wenn Sie das Argument *ActiveConnection* der [Open](open-method-ado-recordset.md) -Methode verwenden, um ein **Recordset** -Objekt zu öffnen, erbt die **ActiveConnection** -Eigenschaft den Wert des Arguments.

Wenn Sie die **Source** -Eigenschaft des **Recordset** -Objekts auf eine gültige **Command** -Objektvariable festlegen, erbt die **ActiveConnection** -Eigenschaft des **Recordset** -Objekts die Einstellung der **ActiveConnection** -Eigenschaft des **Command** -Objekts.

**Remote Data Service-Verwendung** Wenn für ein clientseitiges Recordset-Objekt verwendet wird, kann diese Eigenschaft nur für eine Verbindungszeichenfolge oder (in Microsoft Visual Basic oder Visual Basic Scripting Edition) auf *Nothing*festgelegt werden.

**Record**

Diese Eigenschaft weist Lese-/Schreibzugriff auf, wenn das **Record** -Objekt geschlossen ist, und kann eine Verbindungszeichenfolge oder einen Verweis auf ein geöffnetes **Connection** -Objekt enthalten. Diese Eigenschaft ist schreibgeschützt, wenn das **Record** -Objekt geöffnet ist, und enthält einen Verweis auf ein geöffnetes **Connection** -Objekt.

Ein **Connection** -Objekt wird implizit erstellt, wenn das **Record** -Objekt über eine URL geöffnet wird. Öffnen Sie das **Record** -Objekt mit einem vorhandenen, geöffneten **Connection** -Objekt, indem Sie dem **Connection** -Objekt diese Eigenschaft zuweisen, oder mithilfe des **Connection** -Objekts als Parameter im Aufruf der [Open](open-method-ado-record.md)-Methode. Falls das **Record** -Objekt aus einem vorhandenen **Record** - oder [Recordset](recordset-object-ado.md)-Objekt geöffnet wird, wird es automatisch dem **Connection** -Objekt dieses **Record** - oder **Recordset** -Objekts zugeordnet.


> [!NOTE]
> <P>[!HINWEIS] Für URLs, die das HTTP-Schema verwenden, wird automatisch der <A href="microsoft-ole-db-provider-for-internet-publishing.md">Microsoft OLE DB-Anbieter für Internet Publishing</A> aufgerufen. Weitere Informationen finden Sie unter <A href="absolute-and-relative-urls.md">Absolute and Relative URLs</A>.</P>


