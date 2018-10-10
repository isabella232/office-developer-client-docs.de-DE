---
title: Der OLE DB-Anbieter für Internet Publishing
TOCTitle: The OLE DB Provider for Internet Publishing
ms:assetid: 864e5ece-0f50-5d88-4c40-f951b2a2eded
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249583(v=office.15)
ms:contentKeyID: 48546082
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f9f8fbed638c07e55b3ecb1730633dceee2b5c7e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25473039"
---
# <a name="the-ole-db-provider-for-internet-publishing"></a><span data-ttu-id="9e058-102">Der OLE DB-Anbieter für Internet Publishing</span><span class="sxs-lookup"><span data-stu-id="9e058-102">The OLE DB Provider for Internet Publishing</span></span>


<span data-ttu-id="9e058-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9e058-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9e058-p101">Die ADO-Objekte [Record](record-object-ado.md) und [Stream](stream-object-ado.md) können mit dem Microsoft OLE DB-Anbieter für Internet Publishing (Internet Publishing-Anbieter) verwendet werden, um auf Ressourcen (z. B. Webordner oder von Microsoft FrontPage bediente Dateien) zuzugreifen oder Ressourcen zu bearbeiten. Mit ADO können Sie die Quelle eines **Record** -, **Stream** - oder [Recordset](recordset-object-ado.md)-Objekts als URL angeben. Anschließend können Sie Ressourcen hochladen, herunterladen, verschieben, kopieren oder löschen oder Ressourceneigenschaften direkt bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="9e058-p101">The ADO [Record](record-object-ado.md) and [Stream](stream-object-ado.md) objects can be used with the Microsoft OLE DB Provider for Internet Publishing (Internet Publishing Provider) to access and manipulate resources, such as Web folders or files served by Microsoft FrontPage. With ADO, you can specify the source of a **Record**, **Stream**, or [Recordset](recordset-object-ado.md) to be a URL. You can then upload, download, move, copy, and delete resources, or directly manipulate resource properties.</span></span>

<span data-ttu-id="9e058-107">Beispielcode, bei dem die Objekte **Record** und **Stream** mit dem Internet Publishing-Anbieter verwendet werden, finden Sie unter [Internet Publishing-Szenario](internet-publishing-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="9e058-107">For example code using **Records** and **Streams** with the Internet Publishing Provider, see the [Internet Publishing Scenario](internet-publishing-scenario.md).</span></span>

<span data-ttu-id="9e058-p102">Der Internet Publishing-Anbieter wird mit Microsoft Windows 2000 installiert. Frühere Versionen des Internet Publishing-Anbieters sind auch mit Microsoft Office 2000 und Microsoft Internet Explorer 5.0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9e058-p102">The Internet Publishing Provider is installed with Microsoft Windows 2000. Earlier versions of the Internet Publishing Provider are also available with Microsoft Office 2000 and Microsoft Internet Explorer 5.0.</span></span>

<span data-ttu-id="9e058-110">Sie haben drei Möglichkeiten, ADO mit dem Internet Publishing-Anbieter zu verbinden:</span><span class="sxs-lookup"><span data-stu-id="9e058-110">There are three ways to connect ADO to the Internet Publishing Provider:</span></span>

- <span data-ttu-id="9e058-p103">Geben Sie "URL=" in der Verbindungszeichenfolge an. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9e058-p103">Specify "URL=" in the connection string. For example:</span></span>
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- <span data-ttu-id="9e058-p104">Geben Sie Msdaipp.dso für das Schlüsselwort Provider der Verbindungszeichenfolge an. Beispiel:
</span><span class="sxs-lookup"><span data-stu-id="9e058-p104">Specify Msdaipp.dso for the *Provider* keyword of the connection string. For example:</span></span>
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- <span data-ttu-id="9e058-p105">Geben Sie Msdaipp.dso für die Provider-Eigenschaft des Connection-Objekts an. Beispiel:
</span><span class="sxs-lookup"><span data-stu-id="9e058-p105">Specify Msdaipp.dso for the [Provider](provider-property-ado.md) property of the [Connection](connection-object-ado.md) object. For example:</span></span>
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```


> [!NOTE]
> <P><span data-ttu-id="9e058-p106">Wenn Msdaipp.dso ausdrücklich als Wert für den Anbieter angegeben ist (mit dem Schlüsselwort Provider der Verbindungszeichenfolge oder mit der Provider-Eigenschaft) kann "URL=" nicht in der Verbindungszeichenfolge verwendet werden, da sonst ein Fehler auftritt. Geben Sie die URL stattdessen wie oben dargestellt an.</span><span class="sxs-lookup"><span data-stu-id="9e058-p106">If Msdaipp.dso is explicitly specified as the value of the provider, either with the <EM>Provider</EM> connection string keyword or the <STRONG>Provider</STRONG> property, you cannot use "URL=" in the connection string. If you do, an error will occur. Instead, simply specify the URL as shown above.</span></span></P>



<span data-ttu-id="9e058-120">Weitere Informationen zum Internet Publishing-Anbieter finden Sie unter [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) oder in der Dokumentation zum Anbieter der Quellanwendung, mit der der OLE DB-Anbieter für Internet Publishing installiert wurde: Windows 2000, Office 2000 oder Internet Explorer 5.0.</span><span class="sxs-lookup"><span data-stu-id="9e058-120">For more specific information about the Internet Publishing Provider, see [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), or the provider documentation provided with the source application with which the OLE DB Provider for Internet Publishing was installed: Windows 2000, Office 2000, or Internet Explorer 5.0.</span></span>

