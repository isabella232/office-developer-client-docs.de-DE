---
title: Microsoft OLE DB-Anbieter für Internet Publishing
TOCTitle: Microsoft OLE DB Provider for Internet Publishing
ms:assetid: 5d1e8db5-dabb-0914-e11e-e2eac72bfa77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249327(v=office.15)
ms:contentKeyID: 48545100
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c6f1c7c65d0ac1dd2a6d3ea132a31955f175bc7f
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997483"
---
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a><span data-ttu-id="e6a7e-102">Microsoft OLE DB-Anbieter für Internet Publishing</span><span class="sxs-lookup"><span data-stu-id="e6a7e-102">Microsoft OLE DB Provider for Internet Publishing</span></span>

<span data-ttu-id="e6a7e-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e6a7e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e6a7e-p101">Der Microsoft OLE DB-Anbieter für Internet Publishing ermöglicht ADO den Zugriff auf Ressourcen, die von Microsoft FrontPage oder Microsoft Internet Information Server bedient werden. Zu den Ressourcen zählen Webquelldateien wie HTML-Dateien oder Windows 2000-Webordner.</span><span class="sxs-lookup"><span data-stu-id="e6a7e-p101">The Microsoft OLE DB Provider for Internet Publishing allows ADO to access resources served by Microsoft FrontPage or Microsoft Internet Information Server. Resources include web source files such as HTML files, or Windows 2000 web folders.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="e6a7e-106">Verbindungszeichenfolgen-Parameter</span><span class="sxs-lookup"><span data-stu-id="e6a7e-106">Connection string parameters</span></span>

<span data-ttu-id="e6a7e-107">Um eine Verbindung mit diesem Anbieter herzustellen, legen Sie das *Provider* -Argument der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft fest auf:</span><span class="sxs-lookup"><span data-stu-id="e6a7e-107">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAIPP.DSO 
```

<span data-ttu-id="e6a7e-108">Dieser Wert kann auch mithilfe der [Provider](provider-property-ado.md)-Eigenschaft gesetzt oder gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="e6a7e-108">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="e6a7e-109">Typische Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e6a7e-109">Typical connection string</span></span>

<span data-ttu-id="e6a7e-110">Eine typische Verbindungszeichenfolge für diesen Anbieter lautet:</span><span class="sxs-lookup"><span data-stu-id="e6a7e-110">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="e6a7e-111">\-oder -</span><span class="sxs-lookup"><span data-stu-id="e6a7e-111">\-or-</span></span>

```vb 
 
"URL=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="e6a7e-112">Die Zeichenfolge besteht aus den folgenden Schlüsselwörtern:</span><span class="sxs-lookup"><span data-stu-id="e6a7e-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e6a7e-113">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="e6a7e-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="e6a7e-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e6a7e-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e6a7e-115"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="e6a7e-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="e6a7e-116">Gibt den OLE DB-Anbieter für Internet Publishing an.</span><span class="sxs-lookup"><span data-stu-id="e6a7e-116">Specifies the OLE DB Provider for Internet Publishing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6a7e-117"><strong>Data Source</strong> -oder- <strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="e6a7e-117"><strong>Data Source</strong> -or- <strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="e6a7e-118">Gibt die URL einer Datei oder das Verzeichnis in einem Webordner veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="e6a7e-118">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e6a7e-119"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="e6a7e-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="e6a7e-120">Gibt den Benutzernamen an.</span><span class="sxs-lookup"><span data-stu-id="e6a7e-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e6a7e-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="e6a7e-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="e6a7e-122">Gibt das Benutzerkennwort an.</span><span class="sxs-lookup"><span data-stu-id="e6a7e-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e6a7e-p102">Wenn Sie für den *ResourceURL*-Wert aus "URL=" in der Verbindungszeichenfolge einen ungültigen Wert festlegen, zeigt der Anbieter für Internet Publishing standardmäßig ein Dialogfeld an und fordert zur Eingabe eines gültigen Werts auf. Dies ist ein unerwünschtes Verhalten für eine Komponente auf der mittleren Ebene einer Anwendung, da es die Ausführung des Programms unterbricht, bis das Dialogfeld geschlossen wird. Der Client scheint zu blockieren, weil er von der Komponente keine Antwort erhält.</span><span class="sxs-lookup"><span data-stu-id="e6a7e-p102">If you set the *ResourceURL* value from the "URL=" in the connection string to an invalid value, by default the Internet Publishing Provider raises a dialog box to prompt for a valid value. This is undesirable behavior for a component in the middle tier of an application, because it suspends program execution until the dialog box is cleared and the client appears to freeze because it has not received a response from the component.</span></span>

> [!NOTE]
> <span data-ttu-id="e6a7e-125">Wenn MSDAIPP. DSO explizit angegeben wird, als Wert des Anbieters, entweder mit dem *Anbieter* Verbindungszeichenfolgen-Schlüsselworts oder der **Provider** -Eigenschaft kann nicht verwendet werden "URL =" in der Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e6a7e-125">If MSDAIPP.DSO is explicitly specified as the value of the provider, either with the *Provider* connection string keyword or the **Provider** property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="e6a7e-126">Wenn "URL=" dennoch verwendet wird, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="e6a7e-126">If you do, an error will occur.</span></span> <span data-ttu-id="e6a7e-127">Geben Sie stattdessen einfach die URL an, wie im Thema [Verwenden von ADO mit dem OLE DB-Anbieter für Internet Publishing](the-ole-db-provider-for-internet-publishing.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e6a7e-127">Instead, simply specify the URL as shown in the topic [Using ADO with the OLE DB Provider for Internet Publishing](the-ole-db-provider-for-internet-publishing.md).</span></span>

