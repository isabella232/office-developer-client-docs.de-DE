---
title: Save-Methode - ActiveX Data Objects (ADO)
TOCTitle: Save Method (ADO)
ms:assetid: 02dab13b-f947-b96d-46ea-0def3ed8f28f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248793(v=office.15)
ms:contentKeyID: 48542968
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b4e3698043c109a8f0fbf32c5c2b8c8ae20e824
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875981"
---
# <a name="save-method-ado"></a>Save-Methode (ADO)


**Betrifft**: Access 2013, Office 2013

Speichert das [Recordset](recordset-object-ado.md)-Objekt in einer Datei oder in einem [Stream](stream-object-ado.md)-Objekt.

## <a name="syntax"></a>Syntax

*Recordset-Objekt*. *Ziel*, *PersistFormat* speichern

## <a name="parameters"></a>Parameter

  - *Destination*

  - Optional. Ein **Variant** -Wert, der den vollständigen Namen des Pfads, unter dem das **Recordset** -Objekt gespeichert werden soll, oder einen Verweis auf ein **Stream** -Objekt darstellt.

  - *PersistFormat*

  - Optional. Ein [PersistFormatEnum](persistformatenum.md)-Wert, der das Format angibt, in dem das **Recordset** -Objekt gespeichert werden soll (XML oder ADTG). Der Standardwert lautet **adPersistADTG**.

## <a name="remarks"></a>Hinweise

Die **Save**-Methode kann nur für ein offenes **Recordset**-Objekt aufgerufen werden. Verwenden Sie die [Open](open-method-ado-recordset.md)-Methode, um das **Recordset**-Objekt zu einem späteren Zeitpunkt von der *Destination* wiederherzustellen.

Wenn die [Filter](filter-property-ado.md) -Eigenschaft für das **Recordset-Objekt**gültig ist, werden nur die unter dem Filter zugänglichen Zeilen gespeichert. Wenn das **Recordset** hierarchische ist, werden dann das aktuelle untergeordnete **Recordset-Objekt** und seine untergeordneten Elemente gespeichert, einschließlich des übergeordneten **Recordset-Objekt**. Falls die **Save** -Methode eines untergeordneten **Recordset** -Objekts aufgerufen wird, werden das untergeordnete Element und alle ihm untergeordneten Elemente gespeichert, das übergeordnete Element jedoch nicht.

Wenn Sie das **Recordset**-Objekt das erste Mal speichern, können Sie optional das *Ziel* angeben. Wenn Sie das *Ziel* auslassen, wird eine neue Datei erstellt, deren Namen auf den Wert der [Source](source-property-ado-recordset.md)-Eigenschaft des **Recordset**-Objekts festgelegt ist.

Geben Sie *Ziel* , wenn Sie anschließend nach dem ersten Speichern **Speichern aufrufen** oder, tritt ein Laufzeitfehler auf. Wenn Sie später mit einem neuen *Ziel* **Speichern** aufrufen, wird das **Recordset-Objekt** für den neuen Pfad gespeichert. Das neue Ziel und das ursprüngliche Ziel sind jedoch beide geöffnet.

**Save** schließt das **Recordset**-Objekt oder die *Destination* nicht. Daher können Sie weiterhin mit dem **Recordset**-Objekt arbeiten und Ihre aktuellsten Änderungen speichern. *Destination* bleibt offen, bis das **Recordset**-Objekt geschlossen ist.

Aus Sicherheitsgründen gestattet die **Save** -Methode nur die Verwendung niedriger und benutzerdefinierter Sicherheitseinstellungen in einem von Microsoft Internet Explorer ausgeführten Skript. Ausführlichere Erläuterungen zu Sicherheitsproblemen finden Sie unter "ADO- und RDS-Sicherheitsprobleme in Microsoft Internet Explorer" (in englischer Sprache) im Abschnitt "ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles".

Wenn die **Save** -Methode während eines asynchronen Abruf-, Ausführungs- oder Aktualisierungsvorgangs des **Recordset** -Objekts aufgerufen wird, wartet die **Save** -Methode, bis der asynchrone Vorgang abgeschlossen ist.

Datensätze werden beginnend bei der ersten Zeile des **Recordset** -Objekts gespeichert. Wenn die **Save** -Methode abgeschlossen ist, wird die aktuelle Zeilenposition an die erste Zeile des **Recordset** -Objekts verschoben.

Legen Sie die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft mithilfe von **Save** auf **adUseClient** fest, um optimale Ergebnisse zu erzielen. Wenn Ihr Anbieter nicht die gesamte zum Speichern von **Recordset** -Objekten erforderliche Funktionalität unterstützt, bietet der Cursordienst diese Funktionalität.

Wenn ein **Recordset** -Objekt mit der auf **adUseServer** festgelegten **CursorLocation** -Eigenschaft gespeichert wird, ist die Aktualisierungsfunktion für das **Recordset** -Objekt beschränkt. Je nach der Funktionalität des Anbieters ist in der Regel ist nur das Aktualisieren, Einfügen und Löschen einer einzelnen Tabelle zulässig. Die [Resync](resync-method-ado.md)-Methode ist bei dieser Konfiguration ebenfalls nicht verfügbar.


> [!NOTE]
> <P>[!HINWEIS] Das Speichern eines <STRONG>Recordset</STRONG> -Objekt mit <STRONG>Fields</STRONG> vom Typ <STRONG>adVariant</STRONG>, <STRONG>adIDispatch</STRONG> oder <STRONG>adIUnknown</STRONG> wird von ADO nicht unterstützt und kann zu unvorhersehbaren Ergebnissen führen.</P>



Nur **Filter** in der Form von Kriterienzeichenfolgen (z. B. Bestelldatum \> ' 12/31/1999 ') wirken sich auf den Inhalt eines permanenten **Recordset-Objekt**. Filter mit einem Array von **Lesezeichen** erstellt oder mithilfe eines Werts aus der **FilterGroupEnum** wirkt sich nicht auf den Inhalt des gespeicherten **Recordset-Objekt**aus. Diese Regeln gelten für **Recordsets** mit clientseitige oder serverseitige Cursor erstellt wurden.

Da *der Zielparameter* jedes Objekt, die die OLE DB IStream-Schnittstelle unterstützt akzeptieren kann, können Sie ein **Recordset-Objekt** direkt auf das ASP-Response-Objekt speichern. Weitere Einzelheiten finden Sie unter [Speicherszenario für XML-Recordset](xml-recordset-persistence-scenario.md).

Sie können ein **Recordset** -Objekt im XML-Format auch in einer Instanz eines MSXML DOM-Objekts speichern. Dies wird im folgenden Visual Basic-Code dargestellt:


> [!NOTE]
> <P>[!HINWEIS] Beim Speichern hierarchischer <STRONG>Recordset</STRONG> -Objekte (Datenformen) im XML-Format gelten zwei Einschränkungen. Wenn das hierarchische <STRONG>Recordset</STRONG> -Objekt ausstehende Aktualisierungen enthält, können Sie dieses nicht im XML-Format speichern. Ein parametrisiertes, hierarchisches <STRONG>Recordset</STRONG> -Objekt kann auch nicht gespeichert werden.</P>



Ein im XML-Format gespeichertes Recordset-Objekt wird im UTF-8-Format gespeichert. Wird eine solche Datei in ein Stream-Objekt in ADO geladen, öffnen das Stream-Objekt nur dann ein Recordset-Objekt aus dem Datenstrom, wenn die Charset-Eigenschaft des Datenstroms auf den entsprechenden Wert für das UTF-8-Format festgelegt ist.

