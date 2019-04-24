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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314056"
---
# <a name="ole-db-provider-for-internet-publishing"></a><span data-ttu-id="ca34c-102">OLE DB-Anbieter für Internet Publishing</span><span class="sxs-lookup"><span data-stu-id="ca34c-102">OLE DB Provider for Internet Publishing</span></span>

<span data-ttu-id="ca34c-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca34c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ca34c-104">Die ADO-Objekte [Record](record-object-ado.md) und [Stream](stream-object-ado.md) können zusammen mit dem Microsoft OLE DB-Anbieter für Internet Publishing (Internet Publishing Provider) zum Zugreifen auf und Bearbeiten von Ressourcen wie Webordnern oder Dateien verwendet werden, die von Microsoft FrontPage bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ca34c-104">The ADO [Record](record-object-ado.md) and [Stream](stream-object-ado.md) objects can be used with the Microsoft OLE DB Provider for Internet Publishing (Internet Publishing Provider) to access and manipulate resources, such as web folders or files served by Microsoft FrontPage.</span></span> <span data-ttu-id="ca34c-105">Mit ADO können Sie die Quelle eines **Record**-, **Stream**- oder [Recordset](recordset-object-ado.md)-Objekts als URL angeben.</span><span class="sxs-lookup"><span data-stu-id="ca34c-105">With ADO, you can specify the source of a **Record**, **Stream**, or [Recordset](recordset-object-ado.md) to be a URL.</span></span> <span data-ttu-id="ca34c-106">Anschließend können Sie Ressourcen hochladen, herunterladen, verschieben, kopieren oder löschen oder Ressourceneigenschaften direkt bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="ca34c-106">You can then upload, download, move, copy, and delete resources, or directly manipulate resource properties.</span></span>

<span data-ttu-id="ca34c-107">Beispielcode, bei dem die Objekte **Record** und **Stream** mit dem Internet Publishing-Anbieter verwendet werden, finden Sie unter [Internet Publishing-Szenario](internet-publishing-scenario.md).</span><span class="sxs-lookup"><span data-stu-id="ca34c-107">For example code using **Records** and **Streams** with the Internet Publishing Provider, see the [Internet Publishing Scenario](internet-publishing-scenario.md).</span></span>

<span data-ttu-id="ca34c-p102">Der Internet Publishing-Anbieter wird mit Microsoft Windows 2000 installiert. Frühere Versionen des Internet Publishing-Anbieters sind auch mit Microsoft Office 2000 und Microsoft Internet Explorer 5.0 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ca34c-p102">The Internet Publishing Provider is installed with Microsoft Windows 2000. Earlier versions of the Internet Publishing Provider are also available with Microsoft Office 2000 and Microsoft Internet Explorer 5.0.</span></span>

<span data-ttu-id="ca34c-110">Sie haben drei Möglichkeiten, ADO mit dem Internet Publishing-Anbieter zu verbinden:</span><span class="sxs-lookup"><span data-stu-id="ca34c-110">There are three ways to connect ADO to the Internet Publishing Provider:</span></span>

- <span data-ttu-id="ca34c-p103">Geben Sie "URL=" in der Verbindungszeichenfolge an. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ca34c-p103">Specify "URL=" in the connection string. For example:</span></span>
    
  ```vb 
     
    objConn.Open "URL=https://servername" 
  ```

- <span data-ttu-id="ca34c-113">Geben Sie msdaipp. DSO für das Schlüsselwort *Provider* der Verbindungszeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="ca34c-113">Specify Msdaipp.dso for the *Provider* keyword of the connection string.</span></span> <span data-ttu-id="ca34c-114">For example:</span><span class="sxs-lookup"><span data-stu-id="ca34c-114">For example:</span></span>
    
  ```vb 
     
    objConn.Open "provider=MSDAIPP.DSO;data source=https://servername" 
  ```

- <span data-ttu-id="ca34c-115">Specify Msdaipp.dso for the [Provider](provider-property-ado.md) property of the [Connection](connection-object-ado.md) object.</span><span class="sxs-lookup"><span data-stu-id="ca34c-115">Specify Msdaipp.dso for the [Provider](provider-property-ado.md) property of the [Connection](connection-object-ado.md) object.</span></span> <span data-ttu-id="ca34c-116">For example:</span><span class="sxs-lookup"><span data-stu-id="ca34c-116">For example:</span></span>
    
  ```vb 
     
    objConn.Provider = "MSDAIPP.DSO" 
    objConn.Open "https://servername" 
  ```

> [!NOTE]
> <span data-ttu-id="ca34c-117">Wenn msdaipp. DSO explizit als Wert des Anbieters angegeben wird, entweder mit dem Schlüsselwort *Anbieter* Connection String oder der **Provider** -Eigenschaft, können Sie "URL =" nicht in der Verbindungszeichenfolge verwenden.</span><span class="sxs-lookup"><span data-stu-id="ca34c-117">If Msdaipp.dso is explicitly specified as the value of the provider, either with the *Provider* connection string keyword or the **Provider** property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="ca34c-118">If you do, an error will occur.</span><span class="sxs-lookup"><span data-stu-id="ca34c-118">If you do, an error will occur.</span></span> <span data-ttu-id="ca34c-119">Geben Sie stattdessen einfach die URL an, wie weiter oben in diesem Thema gezeigt.</span><span class="sxs-lookup"><span data-stu-id="ca34c-119">Instead, simply specify the URL as shown earlier in this topic.</span></span>

<span data-ttu-id="ca34c-120">Weitere Informationen zum Internet Publishing-Anbieter finden Sie unter [Microsoft OLE DB-Anbieter für Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md) oder in der Dokumentation zum Anbieter der Quellanwendung, mit der der OLE DB-Anbieter für Internet Publishing installiert wurde: Windows 2000, Office 2000 oder Internet Explorer 5.0.</span><span class="sxs-lookup"><span data-stu-id="ca34c-120">For more specific information about the Internet Publishing Provider, see [Microsoft OLE DB Provider for Internet Publishing](microsoft-ole-db-provider-for-internet-publishing.md), or the provider documentation provided with the source application with which the OLE DB Provider for Internet Publishing was installed: Windows 2000, Office 2000, or Internet Explorer 5.0.</span></span>

