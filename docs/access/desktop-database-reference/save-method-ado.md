---
title: Save-Methode – ActiveX Data Objects (ADO)
TOCTitle: Save method (ADO)
ms:assetid: 02dab13b-f947-b96d-46ea-0def3ed8f28f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248793(v=office.15)
ms:contentKeyID: 48542968
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: de794cac384b31fd2f81f8f2232c6119b862c927
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631720"
---
# <a name="save-method-ado"></a>Save-Methode (ADO)

**Gilt für**: Access 2013, Office 2013

Speichert das [Recordset](recordset-object-ado.md)-Objekt in einer Datei oder in einem [Stream](stream-object-ado.md)-Objekt.

## <a name="syntax"></a>Syntax

*Recordset*. *Save Destination*, *PersistFormat*

## <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:--------|:----------|
|*Destination* |Optional. Ein **Variant** -Wert, der den vollständigen Namen des Pfads, unter dem das **Recordset** -Objekt gespeichert werden soll, oder einen Verweis auf ein **Stream** -Objekt darstellt.|
|*PersistFormat* |Optional. Ein [PersistFormatEnum](persistformatenum.md)-Wert, der das Format angibt, in dem das **Recordset** -Objekt gespeichert werden soll (XML oder ADTG). Der Standardwert lautet **adPersistADTG**.|

## <a name="remarks"></a>Bemerkungen

Die **Save**-Methode kann nur für ein offenes **Recordset**-Objekt aufgerufen werden. Verwenden Sie die [Open](open-method-ado-recordset.md)-Methode, um das **Recordset**-Objekt zu einem späteren Zeitpunkt von der *Destination* wiederherzustellen.

If the [Filter](filter-property-ado.md) property is in effect for the **Recordset**, then only the rows accessible under the filter are saved. If the **Recordset** is hierarchical, then the current child **Recordset** and its children are saved, including the parent **Recordset**. If the **Save** method of a child **Recordset** is called, the child and all its children are saved, but the parent is not.

Wenn Sie das **Recordset**-Objekt das erste Mal speichern, können Sie optional das *Ziel* angeben. Wenn Sie das *Ziel* auslassen, wird eine neue Datei erstellt, deren Namen auf den Wert der [Source](source-property-ado-recordset.md)-Eigenschaft des **Recordset**-Objekts festgelegt ist.

Geben Sie die *Destination* nicht an, wenn Sie nach dem ersten Speichern **Save** aufrufen, andernfalls tritt ein Fehler auf. Wenn Sie nach dem Speichern **Save** mit einer neuen *Destination* aufrufen, wird das **Recordset**-Objekt an diesem neuen Ziel gespeichert. Das neue und das ursprüngliche Ziel sind jedoch beide offen.

**Save** schließt das **Recordset**-Objekt oder die *Destination* nicht. Daher können Sie weiterhin mit dem **Recordset**-Objekt arbeiten und Ihre aktuellsten Änderungen speichern. *Destination* bleibt offen, bis das **Recordset**-Objekt geschlossen ist.

For reasons of security, the **Save** method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer. For a more detailed explanation of security issues, see "ADO and RDS Security Issues in Microsoft Internet Explorer" under ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles.

Wenn die **Save** -Methode während eines asynchronen Abruf-, Ausführungs- oder Aktualisierungsvorgangs des **Recordset** -Objekts aufgerufen wird, wartet die **Save** -Methode, bis der asynchrone Vorgang abgeschlossen ist.

Datensätze werden beginnend bei der ersten Zeile des **Recordset** -Objekts gespeichert. Wenn die **Save** -Methode abgeschlossen ist, wird die aktuelle Zeilenposition an die erste Zeile des **Recordset** -Objekts verschoben.

Legen Sie die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft mithilfe von **Save** auf **adUseClient** fest, um optimale Ergebnisse zu erzielen. Wenn Ihr Anbieter nicht die gesamte zum Speichern von **Recordset** -Objekten erforderliche Funktionalität unterstützt, bietet der Cursordienst diese Funktionalität.

Wenn ein **Recordset** -Objekt mit der auf **adUseServer** festgelegten **CursorLocation** -Eigenschaft gespeichert wird, ist die Aktualisierungsfunktion für das **Recordset** -Objekt beschränkt. Je nach der Funktionalität des Anbieters ist in der Regel ist nur das Aktualisieren, Einfügen und Löschen einer einzelnen Tabelle zulässig. Die [Resync](resync-method-ado.md)-Methode ist bei dieser Konfiguration ebenfalls nicht verfügbar.

> [!NOTE]
> [!HINWEIS] Das Speichern eines **Recordset** -Objekt mit **Fields** vom Typ **adVariant**, **adIDispatch** oder **adIUnknown** wird von ADO nicht unterstützt und kann zu unvorhersehbaren Ergebnissen führen.

Nur **Filter** in Form von Kriterienzeichenfolgen (z. B. OrderDate \> '31.12.1999') wirken sich auf den Inhalt eines permanenten **Recordsets** aus. Filter, die mit einem Array mit **Bookmarks** oder mithilfe eines Werts aus **FilterGroupEnum** erstellt wurden, wirken sich nicht auf den Inhalt des gespeicherten **Recordset**-Objekts aus. Diese Regeln werden auf **Recordset**-Objekte angewendet, die mit einem clientseitigen oder einem serverseitigen Cursor erstellt wurden.

Da der *Destination*-Parameter alle Objekte akzeptiert, die die OLE DB IStream-Schnittstelle unterstützen, können Sie ein **Recordset**-Objekt direkt im ASP Response-Objekt speichern. Weitere Einzelheiten finden Sie unter [Speicherszenario für XML-Recordset](xml-recordset-persistence-scenario.md).

Sie können ein **Recordset** -Objekt im XML-Format auch in einer Instanz eines MSXML DOM-Objekts speichern. Dies wird im folgenden Visual Basic-Code dargestellt:

> [!NOTE]
> [!HINWEIS] Beim Speichern hierarchischer **Recordset** -Objekte (Datenformen) im XML-Format gelten zwei Einschränkungen. Wenn das hierarchische **Recordset** -Objekt ausstehende Aktualisierungen enthält, können Sie dieses nicht im XML-Format speichern. Ein parametrisiertes, hierarchisches **Recordset** -Objekt kann auch nicht gespeichert werden.

A Recordset saved in XML format is saved using UTF-8 format. When such a file is loaded into an ADO Stream, the Stream object will not attempt to open a Recordset from the stream unless the Charset property of the stream is set to the appropriate value for UTF-8 format.

