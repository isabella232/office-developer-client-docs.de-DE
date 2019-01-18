---
title: DataControl-Objekt (RDS)
TOCTitle: DataControl object (RDS)
ms:assetid: ac430669-7628-696c-c036-b5d35405d788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249801(v=office.15)
ms:contentKeyID: 48547001
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2ffe674f3aa02e5cc8b1f89375ca66b4efa623f2
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709782"
---
# <a name="datacontrol-object-rds"></a><span data-ttu-id="7ec43-102">DataControl-Objekt (RDS)</span><span class="sxs-lookup"><span data-stu-id="7ec43-102">DataControl object (RDS)</span></span>

<span data-ttu-id="7ec43-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7ec43-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7ec43-104">Bindet eine Datenabfrage [Recordset-Objekt](recordset-object-ado.md) an einen oder mehrere Steuerelemente (beispielsweise ein Textfeld, Grid-Steuerelement oder Kombinationsfeld) **die Recordsetdaten** auf einer Webseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7ec43-104">Binds a data query [Recordset](recordset-object-ado.md) to one or more controls (for example, a text box, grid control, or combo box) to display the **Recordset** data on a webpage.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ec43-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ec43-105">Syntax</span></span>

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
    </OBJECT>
```

## <a name="remarks"></a><span data-ttu-id="7ec43-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7ec43-106">Remarks</span></span>

<span data-ttu-id="7ec43-107">Die Klassen-ID für das **RDS.DataControl** -Objekt lautet BD96C556-65A3-11D0-983A-00C04FC29E33.</span><span class="sxs-lookup"><span data-stu-id="7ec43-107">The class ID for the **RDS.DataControl** object is BD96C556-65A3-11D0-983A-00C04FC29E33.</span></span>

> [!NOTE]
> <span data-ttu-id="7ec43-p101">[!HINWEIS] Wenn Sie einen Fehler darüber erhalten, dass ein [RDS.DataSpace](dataspace-object-rds.md)- oder **RDS.DataControl** -Objekt nicht geladen werden kann, sollten Sie sicherstellen, dass Sie die richtige Klassen-ID verwenden. Die Klassen-IDs für diese Objekte wurden seit den Versionen 1.0 und 1.1 geändert.</span><span class="sxs-lookup"><span data-stu-id="7ec43-p101">If you get an error that an [RDS.DataSpace](dataspace-object-rds.md) or **RDS.DataControl** object doesn't load, make sure you are using the correct class ID. The class IDs for these objects have changed from version 1.0 and 1.1.</span></span>

<span data-ttu-id="7ec43-110">Für ein Basisszenario müssen Sie nur die Eigenschaften **SQL**, **Connect** und **Server** des **RDS.DataControl** -Objekts festlegen. Damit wird automatisch das Standard-Geschäftsobjekt namens [RDSServer.DataFactory](datafactory-object-rdsserver.md) aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7ec43-110">For a basic scenario, you need to set only the **SQL**, **Connect**, and **Server** properties of the **RDS.DataControl** object, which will automatically call the default business object, [RDSServer.DataFactory](datafactory-object-rdsserver.md).</span></span>

<span data-ttu-id="7ec43-111">Alle Eigenschaften im **RDS.DataControl** -Objekt sind optional, da benutzerdefinierte Geschäftsobjekte ihre Funktionalität ersetzen können.</span><span class="sxs-lookup"><span data-stu-id="7ec43-111">All the properties in the **RDS.DataControl** are optional because custom business objects can replace their functionality.</span></span>

> [!NOTE]
> <span data-ttu-id="7ec43-112">[!HINWEIS] Wenn Sie mehrere Ergebnisse abfragen, wird nur das erste [Recordset](recordset-object-ado.md)-Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ec43-112">If you query for multiple results, only the first [Recordset](recordset-object-ado.md) is returned.</span></span> <span data-ttu-id="7ec43-113">Wenn mehrere Ergebnismengen erforderlich sind, weisen Sie jeder ein eigenes **DataControl** -Objekt zu.</span><span class="sxs-lookup"><span data-stu-id="7ec43-113">If multiple result sets are needed, assign each to its own **DataControl**.</span></span> 
> 
> <span data-ttu-id="7ec43-114">Ein Beispiel für eine Abfrage für mehrere Ergebnisse folgende möglich: `"Select * from Authors, Select * from Topics"`.</span><span class="sxs-lookup"><span data-stu-id="7ec43-114">An example of a query for multiple results could be the following: `"Select * from Authors, Select * from Topics"`.</span></span>

<span data-ttu-id="7ec43-p103">Wenn Sie das **RDS-DataControl** -Objekt verwenden und der Verbindungsreihenfolge "DFMode=20;" hinzufügen, kann sich die Leistung des Servers beim Aktualisieren von Daten verbessern. Bei dieser Einstellung verwendet das **RDSServer.DataFactory** -Objekt auf dem Server einen weniger ressourcenintensiven Modus. In dieser Konfiguration sind die folgenden Features jedoch nicht verfügbar:</span><span class="sxs-lookup"><span data-stu-id="7ec43-p103">Adding "DFMode=20;" to your connection string when using the **RDS.DataControl** object can improve your server's performance when updating data. With this setting, the **RDSServer.DataFactory** object on the server uses a less resource-intensive mode. However, the following features are not available in this configuration:</span></span>

  - <span data-ttu-id="7ec43-118">Verwenden parametrisierter Abfragen.</span><span class="sxs-lookup"><span data-stu-id="7ec43-118">Using parameterized queries.</span></span>

  - <span data-ttu-id="7ec43-119">Abrufen von Parameter- oder Spalteninformationen vor dem Aufrufen der **Execute** -Methode.</span><span class="sxs-lookup"><span data-stu-id="7ec43-119">Getting parameter or column information before calling the **Execute** method.</span></span>

  - <span data-ttu-id="7ec43-120">Festlegen von **Transact Updates** auf **True**.</span><span class="sxs-lookup"><span data-stu-id="7ec43-120">Setting **Transact Updates** to **True**.</span></span>

  - <span data-ttu-id="7ec43-121">Abrufen von Zeilenstatus.</span><span class="sxs-lookup"><span data-stu-id="7ec43-121">Getting row status.</span></span>

  - <span data-ttu-id="7ec43-122">Aufrufen der [Resync](resync-method-ado.md)-Methode.</span><span class="sxs-lookup"><span data-stu-id="7ec43-122">Calling the [Resync](resync-method-ado.md) method.</span></span>

  - <span data-ttu-id="7ec43-123">Aktualisieren (explizit oder automatisch) mithilfe der [Update Resync](update-resync-property-dynamic-ado.md)-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="7ec43-123">Refreshing (explicitly or automatically) via the [Update Resync](update-resync-property-dynamic-ado.md) property.</span></span>

  - <span data-ttu-id="7ec43-124">Festlegen der Eigenschaften von **Command** oder [Recordset](recordset-sourcerecordset-properties-rds.md).</span><span class="sxs-lookup"><span data-stu-id="7ec43-124">Setting **Command** or [Recordset](recordset-sourcerecordset-properties-rds.md) properties.</span></span>

  - <span data-ttu-id="7ec43-125">Verwenden von **adCmdTableDirect**.</span><span class="sxs-lookup"><span data-stu-id="7ec43-125">Using **adCmdTableDirect**.</span></span>

<span data-ttu-id="7ec43-p104">Das **RDS.DataControl** -Objekt wird standardmäßig im asynchronen Modus ausgeführt. Wenn Ihre Anwendung eine synchrone Ausführung erfordert, legen Sie den [ExecuteOptions](executeoptions-property-rds.md)-Parameter auf den Wert **adcExecSync** und den [FetchOptions](fetchoptions-property-rds.md)-Parameter auf den Wert **adcFetchUpFront** fest (siehe folgendes Beispiel).</span><span class="sxs-lookup"><span data-stu-id="7ec43-p104">The **RDS.DataControl** object runs in asynchronous mode by default. If you require synchronous execution for your application, set the [ExecuteOptions](executeoptions-property-rds.md) parameter equal to **adcExecSync** and the [FetchOptions](fetchoptions-property-rds.md) parameter equal to **adcFetchUpFront**, as shown in the following example.</span></span>

```vb
    <OBJECT CLASSID="clsid:BD96C556-65A3-11D0-983A-00C04FC29E33" 
        ID="DataControl"
       <PARAM NAME="Connect" VALUE="DSN=DSNName;UID=usr;PWD=pw;">
       <PARAM NAME="Server" VALUE="https://awebsrvr">
       <PARAM NAME="SQL" VALUE="QueryText">
       <PARAM NAME="ExecuteOptions" VALUE="1">
       <PARAM NAME="FetchOptions" VALUE="1">
    </OBJECT>
```

<span data-ttu-id="7ec43-p105">Verwenden Sie ein **RDS.DataControl** -Objekt, um die Ergebnisse einer einzelnen Abfrage mit einem oder mehreren visuellen Steuerelementen zu verknüpfen. Sie haben z. B. Code, in dem Sie Kundendaten abfragen, wie Namen, Wohnort, Geburtsort, Alter und Kundenprioritätsstatus. In diesem Fall können Sie den Namen, das Alter und die Region eines Kunden unter Verwendung eines einzigen **RDS.DataControl** -Objekts in drei unterschiedlichen Textfeldern, den Kundenprioritätsstatus in einem Kontrollkästchen und alle Daten in einem Rastersteuerelement anzeigen.</span><span class="sxs-lookup"><span data-stu-id="7ec43-p105">Use one **RDS.DataControl** object to link the results of a single query to one or more visual controls. For example, suppose you code a query requesting customer data such as Name, Residence, Place of Birth, Age, and Priority Customer Status. You can use a single **RDS.DataControl** object to display a customer's Name, Age, and Region in three separate text boxes; Priority Customer Status in a check box; and all the data in a grid control.</span></span>

<span data-ttu-id="7ec43-p106">Verwenden Sie unterschiedliche **RDS.DataControl**-Objekte, um die Ergebnisse von Mehrfachabfragen mit verschiedenen visuellen Steuerelementen zu verknüpfen. Sie verwenden z. B. eine Abfrage, um Informationen über einen Kunden zu erhalten, und eine zweite Abfrage, um Informationen über Waren zu erhalten, die der Kunde gekauft hat. Sie möchten die Ergebnisse der ersten Abfrage in drei Textfeldern und einem Kontrollkästchen anzeigen und die Ergebnisse der zweiten Abfrage in einem Rastersteuerelement. Wenn Sie das Standardgeschäftsobjekt verwenden (**RDSServer.DataFactory**), müssen Sie folgendermaßen vorgehen:</span><span class="sxs-lookup"><span data-stu-id="7ec43-p106">Use different **RDS.DataControl** objects to link the results of multiple queries to different visual controls. For example, suppose you use one query to obtain information about a customer, and a second query to obtain information about merchandise that the customer has purchased. You want to display the results of the first query in three text boxes and one check box, and the results of the second query in a grid control. If you use the default business object (**RDSServer.DataFactory**), you need to do the following:</span></span>

  - <span data-ttu-id="7ec43-135">Hinzufügen von zwei **RDS. DataControl** Objekte auf Ihrer Webseite.</span><span class="sxs-lookup"><span data-stu-id="7ec43-135">Add two **RDS.DataControl** objects to your webpage.</span></span>

  - <span data-ttu-id="7ec43-p107">Erstellen Sie zwei Abfragen, jeweils eine für die SQL-Eigenschaft der beiden RDS.DataControl-Objekte. Ein RDS.DataControl-Objekt enthält eine SQL-Abfrage, die Kundeninformationen abfragt. Das zweite RDS.DataControl-Objekt enthält eine Abfrage, mit der eine Liste der vom Kunden gekauften Waren abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="7ec43-p107">Write two queries, one for each **SQL** property of the two **RDS.DataControl** objects. One **RDS.DataControl** object will contain an SQL query requesting customer information; the second will contain a query requesting a list of merchandise the customer has purchased.</span></span>

  - <span data-ttu-id="7ec43-138">Geben Sie im OBJECT-Tag der beiden gebundenen Steuerelemente den DATAFLD-Wert an, um die Werte für die Daten festzulegen, die in den einzelnen visuellen Steuerelementen angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7ec43-138">In each of the bound controls' OBJECT tags, specify the DATAFLD value to set the values for the data you want to display in each visual control.</span></span>

<span data-ttu-id="7ec43-139">Es gibt keine Beschränkung für die Anzahl der **RDS. DataControl** -Objekten, die über OBJECT-Tags auf einer einzelnen Webseite eingebettet werden können.</span><span class="sxs-lookup"><span data-stu-id="7ec43-139">There is no count restriction on the number of **RDS.DataControl** objects that you can embed via OBJECT tags on a single webpage.</span></span>

<span data-ttu-id="7ec43-140">Beim Definieren der **RDS. DataControl** -Objekts auf einer Webseite, verwenden Sie die Werte ungleich NULL **Höhe** und **Breite** wie etwa 1 (um die Aufnahme der leeren Platz zu vermeiden).</span><span class="sxs-lookup"><span data-stu-id="7ec43-140">When you define the **RDS.DataControl** object on a webpage, use nonzero **Height** and **Width** values such as 1 (to avoid the inclusion of extra space).</span></span>

<span data-ttu-id="7ec43-141">Clientkomponenten von Remote Data Service sind bereits in Internet Explorer 4.0 enthalten. Aus diesem Grund ist es nicht erforderlich, einen CODEBASE-Parameter in das **RDS.DataControl** -Objekttag einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="7ec43-141">Remote Data Service client components are already included as part of Internet Explorer 4.0; therefore, you don't need to include a CODEBASE parameter in your **RDS.DataControl** object tag.</span></span>

<span data-ttu-id="7ec43-142">Mit Internet Explorer 4.0 oder höher, können Sie binden an Daten mithilfe von HTML- und ActiveX-Steuerelemente nur, wenn sie als Steuerelemente für des Apartmentthreading-Modells markiert sind.</span><span class="sxs-lookup"><span data-stu-id="7ec43-142">With Internet Explorer 4.0 or later, you can bind to data by using HTML controls and ActiveX controls only if they are marked as apartment model controls.</span></span>

<span data-ttu-id="7ec43-143">**Microsoft Visual Basic-Benutzer** RDS **. DataControl** wird nur in webbasierten Anwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="7ec43-143">**Microsoft Visual Basic Users** The **RDS.DataControl** is used only in web-based applications.</span></span> <span data-ttu-id="7ec43-144">Eine Visual Basic-Clientanwendung benötigt das Objekt nicht.</span><span class="sxs-lookup"><span data-stu-id="7ec43-144">A Visual Basic client application has no need for it.</span></span>

