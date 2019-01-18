---
title: Der OLE DB-Anbieter für Internet Publishing
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 617dca5ced5410e2023657ea1b0b748066f7843f
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699128"
---
# <a name="ole-db-provider-for-internet-publishing"></a><span data-ttu-id="e93e4-102">OLE DB-Anbieter für Internet Publishing</span><span class="sxs-lookup"><span data-stu-id="e93e4-102">OLE DB Provider for Internet Publishing</span></span>

<span data-ttu-id="e93e4-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e93e4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e93e4-104">Die ADO- [Record](record-object-ado.md) und [Stream](stream-object-ado.md) -Objekten können verwendet werden mit dem Microsoft OLE DB-Anbieter für Internet Publishing (Internet Publishing-Anbieter) aufrufen und Bearbeiten von Ressourcen, wie von Webordnern oder Dateien, die von Microsoft FrontPage bedient.</span><span class="sxs-lookup"><span data-stu-id="e93e4-104">The ADO [Record](record-object-ado.md) and [Stream](stream-object-ado.md) objects can be used with the Microsoft OLE DB Provider for Internet Publishing (Internet Publishing Provider) to access and manipulate resources, such as web folders or files served by Microsoft FrontPage.</span></span> <span data-ttu-id="e93e4-105">Mit ADO können Sie die Quelle der **Datensatz**, **Stream**oder [Recordset-Objekt](recordset-object-ado.md) eine URL sein soll, angeben.</span><span class="sxs-lookup"><span data-stu-id="e93e4-105">With ADO, you can specify the source of a **Record**, **Stream**, or [Recordset](recordset-object-ado.md) to be a URL.</span></span> <span data-ttu-id="e93e4-106">Sie können dann hochladen, herunterladen, verschieben, kopieren, und Löschen von Ressourcen oder Ressourceneigenschaften direkt zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e93e4-106">You can then upload, download, move, copy, and delete resources, or directly manipulate resource properties.</span></span>

<span data-ttu-id="e93e4-107">Beispielcode, bei dem die Objekte **Record** und **Stream** mit dem Internet Publishing-Anbieter verwendet werden, finden Sie unter [Internet Publishing-Szenario](internet-publishing-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="e93e4-107">For example code using **Records** and **Streams** with the Internet Publishing Provider, see the [Internet Publishing Scenario](internet-publishing-scenario.md).</span></span>

<span data-ttu-id="e93e4-p102">Der Internet Publishing-Anbieter wird mit Microsoft Windows 2000 installiert. Frühere Versionen des Internet Publishing-Anbieters sind auch mit Microsoft Office 2000 und Microsoft Internet Explorer 5.0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e93e4-p102">The Internet Publishing Provider is installed with Microsoft Windows 2000. Earlier versions of the Internet Publishing Provider are also available with Microsoft Office 2000 and Microsoft Internet Explorer 5.0.</span></span>

<span data-ttu-id="e93e4-110">Sie haben drei Möglichkeiten, ADO mit dem Internet Publishing-Anbieter zu verbinden:</span><span class="sxs-lookup"><span data-stu-id="e93e4-110">There are three ways to connect ADO to the Internet Publishing Provider:</span></span>

- <span data-ttu-id="e93e4-p103">Geben Sie "URL=" in der Verbindungszeichenfolge an. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e93e4-p103">Specify "URL=" in the connection string. For example:</span></span>
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- <span data-ttu-id="e93e4-p104">Geben Sie Msdaipp.dso für das Schlüsselwort Provider der Verbindungszeichenfolge an. Beispiel:
</span><span class="sxs-lookup"><span data-stu-id="e93e4-p104">Specify Msdaipp.dso for the *Provider* keyword of the connection string. For example:</span></span>
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- <span data-ttu-id="e93e4-p105">Geben Sie Msdaipp.dso für die Provider-Eigenschaft des Connection-Objekts an. Beispiel:
</span><span class="sxs-lookup"><span data-stu-id="e93e4-p105">Specify Msdaipp.dso for the [Provider](provider-property-ado.md) property of the [Connection](connection-object-ado.md) object. For example:</span></span>
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```

> [!NOTE]
> <span data-ttu-id="e93e4-117">Wenn Msdaipp.dso explizit als Wert des Anbieters, mit dem *Anbieter* Verbindungszeichenfolgen-Schlüsselworts oder der **Provider** -Eigenschaft angegeben ist kann nicht verwendet "URL =" in der Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e93e4-117">If Msdaipp.dso is explicitly specified as the value of the provider, either with the *Provider* connection string keyword or the **Provider** property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="e93e4-118">Wenn "URL=" dennoch verwendet wird, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="e93e4-118">If you do, an error will occur.</span></span> <span data-ttu-id="e93e4-119">Geben Sie stattdessen einfach die URL wie weiter oben in diesem Thema dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e93e4-119">Instead, simply specify the URL as shown earlier in this topic.</span></span>

<span data-ttu-id="e93e4-120">Weitere Informationen zum Internet Publishing-Anbieter finden Sie unter [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) oder in der Dokumentation zum Anbieter der Quellanwendung, mit der der OLE DB-Anbieter für Internet Publishing installiert wurde: Windows 2000, Office 2000 oder Internet Explorer 5.0.</span><span class="sxs-lookup"><span data-stu-id="e93e4-120">For more specific information about the Internet Publishing Provider, see [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), or the provider documentation provided with the source application with which the OLE DB Provider for Internet Publishing was installed: Windows 2000, Office 2000, or Internet Explorer 5.0.</span></span>

