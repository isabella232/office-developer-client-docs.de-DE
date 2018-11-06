---
title: SendEmail-Makroaktion
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: a5016500b62a465f21ecab93a6fb66c9e6d514e1
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998840"
---
# <a name="sendemail-macro-action"></a><span data-ttu-id="47469-102">SendEmail-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="47469-102">SendEmail macro action</span></span>

<span data-ttu-id="47469-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47469-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47469-104">Die **SendenEMail** -Aktion sendet eine e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="47469-104">The **SendEmail** action sends an email message.</span></span>

> [!NOTE]
> <span data-ttu-id="47469-105">[!HINWEIS] Die **SendenEMail** -Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="47469-105">The **SendEmail** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="47469-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="47469-106">Setting</span></span>

<span data-ttu-id="47469-107">Die **SendenEMail** -Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="47469-107">The **SendEmail** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="47469-108">Argument</span><span class="sxs-lookup"><span data-stu-id="47469-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="47469-109">Eingabe erforderlich</span><span class="sxs-lookup"><span data-stu-id="47469-109">Required</span></span></p></th>
<th><p><span data-ttu-id="47469-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47469-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47469-111"><strong>An</strong></span><span class="sxs-lookup"><span data-stu-id="47469-111"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="47469-112">Ja</span><span class="sxs-lookup"><span data-stu-id="47469-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="47469-113">Die Empfänger der Nachricht, deren Namen Sie in der Zeile <strong>an</strong> , in der Nachricht aufnehmen möchten. Trennen Sie die Namen die Empfänger, die Sie in diesem Argument (und in den Argumenten <em>Cc</em> und <em>Bcc</em> ) durch ein Semikolon (;) angeben.</span><span class="sxs-lookup"><span data-stu-id="47469-113">The recipients of the message whose names you want to put on the <strong>To</strong> line in the message.Separate the recipient names that you specify in this argument (and in the <em>Cc</em> and <em>Bcc</em> arguments) with a semicolon (;).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47469-114"><strong>Cc</strong></span><span class="sxs-lookup"><span data-stu-id="47469-114"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="47469-115">Nein</span><span class="sxs-lookup"><span data-stu-id="47469-115">No</span></span></p></td>
<td><p><span data-ttu-id="47469-116">Die Empfänger der Nachricht, deren Namen Sie in der Cc aufnehmen möchten (&quot;Carbon Copy, Blindkopie&quot;) Zeile der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="47469-116">The message recipients whose names you want to put on the Cc (&quot;carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47469-117"><strong>Bcc</strong></span><span class="sxs-lookup"><span data-stu-id="47469-117"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="47469-118">Nein</span><span class="sxs-lookup"><span data-stu-id="47469-118">No</span></span></p></td>
<td><p><span data-ttu-id="47469-119">Die Empfänger der Nachricht, deren Namen Sie in der Bcc aufnehmen möchten (&quot;blind Carbon Copy, Blindkopie&quot;) Zeile der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="47469-119">The message recipients whose names you want to put on the Bcc (&quot;blind carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47469-120"><strong>Betreff</strong></span><span class="sxs-lookup"><span data-stu-id="47469-120"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="47469-121">Nein</span><span class="sxs-lookup"><span data-stu-id="47469-121">No</span></span></p></td>
<td><p><span data-ttu-id="47469-p101">Der Betreff der Nachricht. Dieser Text wird auf der Zeile <strong>Betreff</strong> der Nachricht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="47469-p101">The subject of the message. This text appears on the <strong>Subject</strong> line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47469-124"><strong>Body</strong></span><span class="sxs-lookup"><span data-stu-id="47469-124"><strong>Body</strong></span></span></p></td>
<td><p><span data-ttu-id="47469-125">Nein</span><span class="sxs-lookup"><span data-stu-id="47469-125">No</span></span></p></td>
<td><p><span data-ttu-id="47469-p102">Der Text, den Sie im Haupttext der E-Mail-Nachricht eingeben möchten. Wenn Sie dieses Argument leer lassen, wird kein zusätzlicher Text in der Nachricht eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="47469-p102">The text that you want to include in the main body of the mail message. If you leave this argument blank, no additional text is included in the message.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="47469-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="47469-128">Remarks</span></span>

<span data-ttu-id="47469-129">Die **SendenEMail** -Aktion ist nur in den Makroereignissen **[Nach Löschvorgang](after-delete-macro-event.md)**, **[Nach Eingabe](after-insert-macro-event.md)** und **[Nach Aktualisierung](after-update-macro-event.md)** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="47469-129">The **SendEmail** action is available only in the **[After Delete](after-delete-macro-event.md)**, **[After Insert](after-insert-macro-event.md)**, and **[After Update](after-update-macro-event.md)** macro events.</span></span>

<span data-ttu-id="47469-130">Mit der **SendenEMail** -Aktion wird die Nachricht nicht zum Bearbeiten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="47469-130">The **SendEmail** action does not display the message for editing.</span></span>

