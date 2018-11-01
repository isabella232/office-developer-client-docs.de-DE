---
title: Microsoft OLE DB-Anbieter für Internet Publishing
TOCTitle: Microsoft OLE DB Provider for Internet Publishing
ms:assetid: 5d1e8db5-dabb-0914-e11e-e2eac72bfa77
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249327(v=office.15)
ms:contentKeyID: 48545100
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: bb0bb40d0f12bd9d5a6c8b29af1d4e27d806db87
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882084"
---
# <a name="microsoft-ole-db-provider-for-internet-publishing"></a><span data-ttu-id="116bd-102">Microsoft OLE DB-Anbieter für Internet Publishing</span><span class="sxs-lookup"><span data-stu-id="116bd-102">Microsoft OLE DB Provider for Internet Publishing</span></span>

<span data-ttu-id="116bd-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="116bd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="116bd-p101">Der Microsoft OLE DB-Anbieter für Internet Publishing ermöglicht ADO den Zugriff auf Ressourcen, die von Microsoft FrontPage oder Microsoft Internet Information Server bedient werden. Zu den Ressourcen zählen Webquelldateien wie HTML-Dateien oder Windows 2000-Webordner.</span><span class="sxs-lookup"><span data-stu-id="116bd-p101">The Microsoft OLE DB Provider for Internet Publishing allows ADO to access resources served by Microsoft FrontPage or Microsoft Internet Information Server. Resources include web source files such as HTML files, or Windows 2000 web folders.</span></span>

## <a name="connection-string-parameters"></a><span data-ttu-id="116bd-106">Verbindungszeichenfolgen-Parameter</span><span class="sxs-lookup"><span data-stu-id="116bd-106">Connection String Parameters</span></span>

<span data-ttu-id="116bd-107">Um eine Verbindung mit diesem Anbieter herzustellen, legen Sie das *Provider* -Argument der [ConnectionString](connectionstring-property-ado.md)-Eigenschaft fest auf:</span><span class="sxs-lookup"><span data-stu-id="116bd-107">To connect to this provider, set the *Provider* argument of the [ConnectionString](connectionstring-property-ado.md) property to:</span></span>

```vb 
 
MSDAIPP.DSO 
```

<span data-ttu-id="116bd-108">Dieser Wert kann auch mithilfe der [Provider](provider-property-ado.md)-Eigenschaft gesetzt oder gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="116bd-108">This value can also be set or read using the [Provider](provider-property-ado.md) property.</span></span>

## <a name="typical-connection-string"></a><span data-ttu-id="116bd-109">Typische Verbindungszeichenfolge</span><span class="sxs-lookup"><span data-stu-id="116bd-109">Typical Connection String</span></span>

<span data-ttu-id="116bd-110">Eine typische Verbindungszeichenfolge für diesen Anbieter lautet:</span><span class="sxs-lookup"><span data-stu-id="116bd-110">A typical connection string for this provider is:</span></span>

```vb 
 
"Provider=MSDAIPP.DSO;Data Source=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="116bd-111">\-oder -</span><span class="sxs-lookup"><span data-stu-id="116bd-111">\-or-</span></span>

```vb 
 
"URL=ResourceURL;User ID=userName;Password=userPassword;" 
```

<span data-ttu-id="116bd-112">Die Zeichenfolge besteht aus den folgenden Schlüsselwörtern:</span><span class="sxs-lookup"><span data-stu-id="116bd-112">The string consists of these keywords:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="116bd-113">Schlüsselwort</span><span class="sxs-lookup"><span data-stu-id="116bd-113">Keyword</span></span></p></th>
<th><p><span data-ttu-id="116bd-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="116bd-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="116bd-115"><strong>Provider</strong></span><span class="sxs-lookup"><span data-stu-id="116bd-115"><strong>Provider</strong></span></span></p></td>
<td><p><span data-ttu-id="116bd-116">Gibt den OLE DB-Anbieter für Internet Publishing an.</span><span class="sxs-lookup"><span data-stu-id="116bd-116">Specifies the OLE DB Provider for Internet Publishing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="116bd-117"><strong>Data Source</strong> -oder- <strong>URL</strong></span><span class="sxs-lookup"><span data-stu-id="116bd-117"><strong>Data Source</strong> -or- <strong>URL</strong></span></span></p></td>
<td><p><span data-ttu-id="116bd-118">Gibt die URL einer Datei oder das Verzeichnis in einem Webordner veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="116bd-118">Specifies the URL of a file or directory published in a web folder.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="116bd-119"><strong>User ID</strong></span><span class="sxs-lookup"><span data-stu-id="116bd-119"><strong>User ID</strong></span></span></p></td>
<td><p><span data-ttu-id="116bd-120">Gibt den Benutzernamen an.</span><span class="sxs-lookup"><span data-stu-id="116bd-120">Specifies the user name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="116bd-121"><strong>Password</strong></span><span class="sxs-lookup"><span data-stu-id="116bd-121"><strong>Password</strong></span></span></p></td>
<td><p><span data-ttu-id="116bd-122">Gibt das Benutzerkennwort an.</span><span class="sxs-lookup"><span data-stu-id="116bd-122">Specifies the user password.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="116bd-p102">Wenn Sie für den *ResourceURL*-Wert aus "URL=" in der Verbindungszeichenfolge einen ungültigen Wert festlegen, zeigt der Anbieter für Internet Publishing standardmäßig ein Dialogfeld an und fordert zur Eingabe eines gültigen Werts auf. Dies ist ein unerwünschtes Verhalten für eine Komponente auf der mittleren Ebene einer Anwendung, da es die Ausführung des Programms unterbricht, bis das Dialogfeld geschlossen wird. Der Client scheint zu blockieren, weil er von der Komponente keine Antwort erhält.</span><span class="sxs-lookup"><span data-stu-id="116bd-p102">If you set the *ResourceURL* value from the "URL=" in the connection string to an invalid value, by default the Internet Publishing Provider raises a dialog box to prompt for a valid value. This is undesirable behavior for a component in the middle tier of an application, because it suspends program execution until the dialog box is cleared and the client appears to freeze because it has not received a response from the component.</span></span>


> [!NOTE]
> <P><span data-ttu-id="116bd-125">Wenn MSDAIPP. DSO explizit angegeben wird, als Wert des Anbieters, entweder mit dem <EM>Anbieter</EM> Verbindungszeichenfolgen-Schlüsselworts oder der <STRONG>Provider</STRONG> -Eigenschaft kann nicht verwendet werden "URL =" in der Verbindungszeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="116bd-125">If MSDAIPP.DSO is explicitly specified as the value of the provider, either with the <EM>Provider</EM> connection string keyword or the <STRONG>Provider</STRONG> property, you cannot use "URL=" in the connection string.</span></span> <span data-ttu-id="116bd-126">Wenn "URL=" dennoch verwendet wird, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="116bd-126">If you do, an error will occur.</span></span> <span data-ttu-id="116bd-127">Geben Sie stattdessen einfach die URL an, wie im Thema <A href="the-ole-db-provider-for-internet-publishing.md">Verwenden von ADO mit dem OLE DB-Anbieter für Internet Publishing</A> beschrieben.</span><span class="sxs-lookup"><span data-stu-id="116bd-127">Instead, simply specify the URL as shown in the topic <A href="the-ole-db-provider-for-internet-publishing.md">Using ADO with the OLE DB Provider for Internet Publishing</A>.</span></span></P>


