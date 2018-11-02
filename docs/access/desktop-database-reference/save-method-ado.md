---
title: Save-Methode - ActiveX Data Objects (ADO)
TOCTitle: Save method (ADO)
ms:assetid: 02dab13b-f947-b96d-46ea-0def3ed8f28f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248793(v=office.15)
ms:contentKeyID: 48542968
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d779fc5cff955ca669635ca827456dafb8927d8a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919682"
---
# <a name="save-method-ado"></a><span data-ttu-id="bf0ab-102">Save-Methode (ADO)</span><span class="sxs-lookup"><span data-stu-id="bf0ab-102">Save method (ADO)</span></span>


<span data-ttu-id="bf0ab-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bf0ab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bf0ab-104">Speichert das [Recordset](recordset-object-ado.md)-Objekt in einer Datei oder in einem [Stream](stream-object-ado.md)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-104">Saves the [Recordset](recordset-object-ado.md) in a file or [Stream](stream-object-ado.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf0ab-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf0ab-105">Syntax</span></span>

<span data-ttu-id="bf0ab-106">*Recordset-Objekt*. *Ziel*, *PersistFormat* speichern</span><span class="sxs-lookup"><span data-stu-id="bf0ab-106">*recordset*.Save*Destination*, *PersistFormat*</span></span>

## <a name="parameters"></a><span data-ttu-id="bf0ab-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf0ab-107">Parameters</span></span>

  - <span data-ttu-id="bf0ab-108">*Destination*</span><span class="sxs-lookup"><span data-stu-id="bf0ab-108">*Destination*</span></span>

  - <span data-ttu-id="bf0ab-p101">Optional. Ein **Variant** -Wert, der den vollständigen Namen des Pfads, unter dem das **Recordset** -Objekt gespeichert werden soll, oder einen Verweis auf ein **Stream** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-p101">Optional. A **Variant** that represents the complete path name of the file where the **Recordset** is to be saved, or a reference to a **Stream** object.</span></span>

  - <span data-ttu-id="bf0ab-111">*PersistFormat*</span><span class="sxs-lookup"><span data-stu-id="bf0ab-111">*PersistFormat*</span></span>

  - <span data-ttu-id="bf0ab-p102">Optional. Ein [PersistFormatEnum](persistformatenum.md)-Wert, der das Format angibt, in dem das **Recordset** -Objekt gespeichert werden soll (XML oder ADTG). Der Standardwert lautet **adPersistADTG**.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-p102">Optional. A [PersistFormatEnum](persistformatenum.md) value that specifies the format in which the **Recordset** is to be saved (XML or ADTG). The default value is **adPersistADTG**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf0ab-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bf0ab-115">Remarks</span></span>

<span data-ttu-id="bf0ab-p103">Die **Save**-Methode kann nur für ein offenes **Recordset**-Objekt aufgerufen werden. Verwenden Sie die [Open](open-method-ado-recordset.md)-Methode, um das **Recordset**-Objekt zu einem späteren Zeitpunkt von der *Destination* wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-p103">The **Save** method can only be invoked on an open **Recordset**. Use the [Open](open-method-ado-recordset.md) method to later restore the **Recordset** from *Destination*.</span></span>

<span data-ttu-id="bf0ab-118">Wenn die [Filter](filter-property-ado.md) -Eigenschaft für das **Recordset-Objekt**gültig ist, werden nur die unter dem Filter zugänglichen Zeilen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-118">If the [Filter](filter-property-ado.md) property is in effect for the **Recordset**, then only the rows accessible under the filter are saved.</span></span> <span data-ttu-id="bf0ab-119">Wenn das **Recordset** hierarchische ist, werden dann das aktuelle untergeordnete **Recordset-Objekt** und seine untergeordneten Elemente gespeichert, einschließlich des übergeordneten **Recordset-Objekt**.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-119">If the **Recordset** is hierarchical, then the current child **Recordset** and its children are saved, including the parent **Recordset**.</span></span> <span data-ttu-id="bf0ab-120">Falls die **Save** -Methode eines untergeordneten **Recordset** -Objekts aufgerufen wird, werden das untergeordnete Element und alle ihm untergeordneten Elemente gespeichert, das übergeordnete Element jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-120">If the **Save** method of a child **Recordset** is called, the child and all its children are saved, but the parent is not.</span></span>

<span data-ttu-id="bf0ab-p105">Wenn Sie das **Recordset**-Objekt das erste Mal speichern, können Sie optional das *Ziel* angeben. Wenn Sie das *Ziel* auslassen, wird eine neue Datei erstellt, deren Namen auf den Wert der [Source](source-property-ado-recordset.md)-Eigenschaft des **Recordset**-Objekts festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-p105">The first time you save the **Recordset**, it is optional to specify *Destination*. If you omit *Destination*, a new file will be created with a name set to the value of the [Source](source-property-ado-recordset.md) property of the **Recordset**.</span></span>

<span data-ttu-id="bf0ab-123">Geben Sie *Ziel* , wenn Sie anschließend nach dem ersten Speichern **Speichern aufrufen** oder, tritt ein Laufzeitfehler auf.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-123">Omit *Destination* when you subsequently call **Save** after the first save, or a run-time error will occur.</span></span> <span data-ttu-id="bf0ab-124">Wenn Sie später mit einem neuen *Ziel* **Speichern** aufrufen, wird das **Recordset-Objekt** für den neuen Pfad gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-124">If you subsequently call **Save** with a new *Destination*, the **Recordset** is saved to the new destination.</span></span> <span data-ttu-id="bf0ab-125">Das neue Ziel und das ursprüngliche Ziel sind jedoch beide geöffnet.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-125">However, the new destination and the original destination will both be open.</span></span>

<span data-ttu-id="bf0ab-p107">**Save** schließt das **Recordset**-Objekt oder die *Destination* nicht. Daher können Sie weiterhin mit dem **Recordset**-Objekt arbeiten und Ihre aktuellsten Änderungen speichern. *Destination* bleibt offen, bis das **Recordset**-Objekt geschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-p107">**Save** does not close the **Recordset** or *Destination*, so you can continue to work with the **Recordset** and save your most recent changes. *Destination* remains open until the **Recordset** is closed.</span></span>

<span data-ttu-id="bf0ab-p108">Aus Sicherheitsgründen gestattet die **Save** -Methode nur die Verwendung niedriger und benutzerdefinierter Sicherheitseinstellungen in einem von Microsoft Internet Explorer ausgeführten Skript. Ausführlichere Erläuterungen zu Sicherheitsproblemen finden Sie unter "ADO- und RDS-Sicherheitsprobleme in Microsoft Internet Explorer" (in englischer Sprache) im Abschnitt "ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles".</span><span class="sxs-lookup"><span data-stu-id="bf0ab-p108">For reasons of security, the **Save** method permits only the use of low and custom security settings from a script executed by Microsoft Internet Explorer. For a more detailed explanation of security issues, see "ADO and RDS Security Issues in Microsoft Internet Explorer" under ActiveX Data Objects (ADO) Technical Articles in Microsoft Data Access Technical Articles.</span></span>

<span data-ttu-id="bf0ab-130">Wenn die **Save** -Methode während eines asynchronen Abruf-, Ausführungs- oder Aktualisierungsvorgangs des **Recordset** -Objekts aufgerufen wird, wartet die **Save** -Methode, bis der asynchrone Vorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-130">If the **Save** method is called while an asynchronous **Recordset** fetch, execute, or update operation is in progress, then **Save** waits until the asynchronous operation is complete.</span></span>

<span data-ttu-id="bf0ab-p109">Datensätze werden beginnend bei der ersten Zeile des **Recordset** -Objekts gespeichert. Wenn die **Save** -Methode abgeschlossen ist, wird die aktuelle Zeilenposition an die erste Zeile des **Recordset** -Objekts verschoben.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-p109">Records are saved beginning with the first row of the **Recordset**. When the **Save** method is finished, the current row position is moved to the first row of the **Recordset**.</span></span>

<span data-ttu-id="bf0ab-p110">Legen Sie die [CursorLocation](cursorlocation-property-ado.md)-Eigenschaft mithilfe von **Save** auf **adUseClient** fest, um optimale Ergebnisse zu erzielen. Wenn Ihr Anbieter nicht die gesamte zum Speichern von **Recordset** -Objekten erforderliche Funktionalität unterstützt, bietet der Cursordienst diese Funktionalität.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-p110">For best results, set the [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient** with **Save**. If your provider does not support all of the functionality necessary to save **Recordset** objects, the Cursor Service will provide that functionality.</span></span>

<span data-ttu-id="bf0ab-p111">Wenn ein **Recordset** -Objekt mit der auf **adUseServer** festgelegten **CursorLocation** -Eigenschaft gespeichert wird, ist die Aktualisierungsfunktion für das **Recordset** -Objekt beschränkt. Je nach der Funktionalität des Anbieters ist in der Regel ist nur das Aktualisieren, Einfügen und Löschen einer einzelnen Tabelle zulässig. Die [Resync](resync-method-ado.md)-Methode ist bei dieser Konfiguration ebenfalls nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-p111">When a **Recordset** is persisted with the **CursorLocation** property set to **adUseServer**, the update capability for the **Recordset** is limited. Typically, only single-table updates, insertions, and deletions are allowed (dependant upon provider functionality). The [Resync](resync-method-ado.md) method is also unavailable in this configuration.</span></span>


> [!NOTE]
> <P><span data-ttu-id="bf0ab-138">[!HINWEIS] Das Speichern eines <STRONG>Recordset</STRONG> -Objekt mit <STRONG>Fields</STRONG> vom Typ <STRONG>adVariant</STRONG>, <STRONG>adIDispatch</STRONG> oder <STRONG>adIUnknown</STRONG> wird von ADO nicht unterstützt und kann zu unvorhersehbaren Ergebnissen führen.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-138">Saving a <STRONG>Recordset</STRONG> with <STRONG>Fields</STRONG> of type <STRONG>adVariant</STRONG>, <STRONG>adIDispatch</STRONG>, or <STRONG>adIUnknown</STRONG> is not supported by ADO and can cause unpredictable results.</span></span></P>



<span data-ttu-id="bf0ab-139">Nur **Filter** in der Form von Kriterienzeichenfolgen (z. B. Bestelldatum \> ' 12/31/1999 ') wirken sich auf den Inhalt eines permanenten **Recordset-Objekt**.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-139">Only **Filters** in the form of Criteria Strings (e.g. OrderDate \> '12/31/1999') affect the contents of a persisted **Recordset**.</span></span> <span data-ttu-id="bf0ab-140">Filter mit einem Array von **Lesezeichen** erstellt oder mithilfe eines Werts aus der **FilterGroupEnum** wirkt sich nicht auf den Inhalt des gespeicherten **Recordset-Objekt**aus.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-140">Filters created with an Array of **Bookmarks** or using a value from the **FilterGroupEnum** will not affect the contents of the persisted **Recordset**.</span></span> <span data-ttu-id="bf0ab-141">Diese Regeln gelten für **Recordsets** mit clientseitige oder serverseitige Cursor erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-141">These rules apply to **Recordsets** created with either client-side or server-side cursors.</span></span>

<span data-ttu-id="bf0ab-142">Da *der Zielparameter* jedes Objekt, die die OLE DB IStream-Schnittstelle unterstützt akzeptieren kann, können Sie ein **Recordset-Objekt** direkt auf das ASP-Response-Objekt speichern.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-142">Because the *Destination* parameter can accept any object that supports the OLE DB IStream interface, you can save a **Recordset** directly to the ASP Response object.</span></span> <span data-ttu-id="bf0ab-143">Weitere Einzelheiten finden Sie unter [Speicherszenario für XML-Recordset](xml-recordset-persistence-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="bf0ab-143">For more details, please see the [XML Recordset Persistence Scenario](xml-recordset-persistence-scenario.md).</span></span>

<span data-ttu-id="bf0ab-144">Sie können ein **Recordset** -Objekt im XML-Format auch in einer Instanz eines MSXML DOM-Objekts speichern. Dies wird im folgenden Visual Basic-Code dargestellt:</span><span class="sxs-lookup"><span data-stu-id="bf0ab-144">You can also save a **Recordset** in XML format to an instance of an MSXML DOM object, as is shown in the following Visual Basic code:</span></span>


> [!NOTE]
> <P><span data-ttu-id="bf0ab-p114">[!HINWEIS] Beim Speichern hierarchischer <STRONG>Recordset</STRONG> -Objekte (Datenformen) im XML-Format gelten zwei Einschränkungen. Wenn das hierarchische <STRONG>Recordset</STRONG> -Objekt ausstehende Aktualisierungen enthält, können Sie dieses nicht im XML-Format speichern. Ein parametrisiertes, hierarchisches <STRONG>Recordset</STRONG> -Objekt kann auch nicht gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-p114">Two limitations apply when saving hierarchical <STRONG>Recordsets</STRONG> (data shapes) in XML format. You cannot save into XML if the hierarchical <STRONG>Recordset</STRONG> contains pending updates, and you cannot save a parameterized hierarchical <STRONG>Recordset</STRONG>.</span></span></P>



<span data-ttu-id="bf0ab-p115">Ein im XML-Format gespeichertes Recordset-Objekt wird im UTF-8-Format gespeichert. Wird eine solche Datei in ein Stream-Objekt in ADO geladen, öffnen das Stream-Objekt nur dann ein Recordset-Objekt aus dem Datenstrom, wenn die Charset-Eigenschaft des Datenstroms auf den entsprechenden Wert für das UTF-8-Format festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bf0ab-p115">A Recordset saved in XML format is saved using UTF-8 format. When such a file is loaded into an ADO Stream, the Stream object will not attempt to open a Recordset from the stream unless the Charset property of the stream is set to the appropriate value for UTF-8 format.</span></span>

