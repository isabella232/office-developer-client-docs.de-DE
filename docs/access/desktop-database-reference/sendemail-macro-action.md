---
title: SendenEMail-Makroaktion
TOCTitle: SendEmail Macro Action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fb2624a00ed2fdbe4a2b24a1f052e19217a4c1a9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871941"
---
# <a name="sendemail-macro-action"></a><span data-ttu-id="864da-102">SendenEMail-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="864da-102">SendEmail Macro Action</span></span>


<span data-ttu-id="864da-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="864da-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="864da-104">Mit der **SendenEMail** -Aktion senden Sie eine E-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="864da-104">The **SendEmail** action sends an e-mail message.</span></span>


> [!NOTE]
> <P><span data-ttu-id="864da-105">[!HINWEIS] Die <STRONG>SendenEMail</STRONG> -Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="864da-105">The <STRONG>SendEmail</STRONG> action is available only in Data Macros.</span></span></P>



## <a name="setting"></a><span data-ttu-id="864da-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="864da-106">Setting</span></span>

<span data-ttu-id="864da-107">Die **SendenEMail** -Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="864da-107">The **SendEmail** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="864da-108">Argument</span><span class="sxs-lookup"><span data-stu-id="864da-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="864da-109">Eingabe erforderlich</span><span class="sxs-lookup"><span data-stu-id="864da-109">Required</span></span></p></th>
<th><p><span data-ttu-id="864da-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="864da-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="864da-111"><strong>An</strong></span><span class="sxs-lookup"><span data-stu-id="864da-111"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="864da-112">Ja</span><span class="sxs-lookup"><span data-stu-id="864da-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="864da-113">Die Empfänger der Nachricht, deren Namen Sie in der Zeile <strong>an</strong> , in der Nachricht aufnehmen möchten. Trennen Sie die Namen die Empfänger, die Sie in diesem Argument (und in den Argumenten <em>Cc</em> und <em>Bcc</em> ) durch ein Semikolon (;) angeben.</span><span class="sxs-lookup"><span data-stu-id="864da-113">The recipients of the message whose names you want to put on the <strong>To</strong> line in the message.Separate the recipient names that you specify in this argument (and in the <em>Cc</em> and <em>Bcc</em> arguments) with a semicolon (;).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="864da-114"><strong>Cc</strong></span><span class="sxs-lookup"><span data-stu-id="864da-114"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="864da-115">Nein</span><span class="sxs-lookup"><span data-stu-id="864da-115">No</span></span></p></td>
<td><p><span data-ttu-id="864da-116">Die Empfänger der Nachricht, deren Namen Sie in der Cc aufnehmen möchten (&quot;Carbon Copy, Blindkopie&quot;) Zeile der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="864da-116">The message recipients whose names you want to put on the Cc (&quot;carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="864da-117"><strong>Bcc</strong></span><span class="sxs-lookup"><span data-stu-id="864da-117"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="864da-118">Nein</span><span class="sxs-lookup"><span data-stu-id="864da-118">No</span></span></p></td>
<td><p><span data-ttu-id="864da-119">Die Empfänger der Nachricht, deren Namen Sie in der Bcc aufnehmen möchten (&quot;blind Carbon Copy, Blindkopie&quot;) Zeile der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="864da-119">The message recipients whose names you want to put on the Bcc (&quot;blind carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="864da-120"><strong>Betreff</strong></span><span class="sxs-lookup"><span data-stu-id="864da-120"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="864da-121">Nein</span><span class="sxs-lookup"><span data-stu-id="864da-121">No</span></span></p></td>
<td><p><span data-ttu-id="864da-p101">Der Betreff der Nachricht. Dieser Text wird auf der Zeile <strong>Betreff</strong> der Nachricht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="864da-p101">The subject of the message. This text appears on the <strong>Subject</strong> line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="864da-124"><strong>Body</strong></span><span class="sxs-lookup"><span data-stu-id="864da-124"><strong>Body</strong></span></span></p></td>
<td><p><span data-ttu-id="864da-125">Nein</span><span class="sxs-lookup"><span data-stu-id="864da-125">No</span></span></p></td>
<td><p><span data-ttu-id="864da-p102">Der Text, den Sie im Haupttext der E-Mail-Nachricht eingeben möchten. Wenn Sie dieses Argument leer lassen, wird kein zusätzlicher Text in der Nachricht eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="864da-p102">The text that you want to include in the main body of the mail message. If you leave this argument blank, no additional text is included in the message.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="864da-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="864da-128">Remarks</span></span>

<span data-ttu-id="864da-129">Die **SendenEMail** -Aktion ist nur in den Makroereignissen **[Nach Löschvorgang](after-delete-macro-event.md)**, **[Nach Eingabe](after-insert-macro-event.md)** und **[Nach Aktualisierung](after-update-macro-event.md)** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="864da-129">The **SendEmail** action is available only in the **[After Delete](after-delete-macro-event.md)**, **[After Insert](after-insert-macro-event.md)**, and **[After Update](after-update-macro-event.md)** macro events.</span></span>

<span data-ttu-id="864da-130">Mit der **SendenEMail** -Aktion wird die Nachricht nicht zum Bearbeiten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="864da-130">The **SendEmail** action does not display the message for editing.</span></span>

