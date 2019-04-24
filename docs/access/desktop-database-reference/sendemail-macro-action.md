---
title: SendEmail-Makroaktion
TOCTitle: SendEmail macro action
ms:assetid: 84ff6b46-d239-4716-9964-5b909656d347
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196780(v=office.15)
ms:contentKeyID: 48546046
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c0fa220b3088cde46b0e82631c06520afd839c64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314651"
---
# <a name="sendemail-macro-action"></a><span data-ttu-id="0e356-102">SendEmail-Makroaktion</span><span class="sxs-lookup"><span data-stu-id="0e356-102">SendEmail macro action</span></span>

<span data-ttu-id="0e356-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0e356-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0e356-104">Die **sendenemail** -Aktion sendet eine e-Mail-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0e356-104">The **SendEmail** action sends an email message.</span></span>

> [!NOTE]
> <span data-ttu-id="0e356-105">Die **SendenEMail**-Aktion ist nur in Datenmakros verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0e356-105">The **SendEmail** action is available only in Data Macros.</span></span>

## <a name="setting"></a><span data-ttu-id="0e356-106">Einstellung</span><span class="sxs-lookup"><span data-stu-id="0e356-106">Setting</span></span>

<span data-ttu-id="0e356-107">Die **SendenEMail**-Aktion kann mit den folgenden Argumenten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0e356-107">The **SendEmail** action has the following arguments.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0e356-108">Argument</span><span class="sxs-lookup"><span data-stu-id="0e356-108">Argument</span></span></p></th>
<th><p><span data-ttu-id="0e356-109">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="0e356-109">Required</span></span></p></th>
<th><p><span data-ttu-id="0e356-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0e356-110">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e356-111"><strong>Ziel</strong></span><span class="sxs-lookup"><span data-stu-id="0e356-111"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="0e356-112">Ja</span><span class="sxs-lookup"><span data-stu-id="0e356-112">Yes</span></span></p></td>
<td><p><span data-ttu-id="0e356-113">Die Empfänger der Nachricht, deren Namen Sie in der Nachricht an die <strong>an</strong> -Stelle setzen möchten. Trennen Sie die in diesem Argument angegebenen Empfängernamen (und in den Argumenten <em>CC</em> und <em>Bcc</em> ) mit einem Semikolon (;).</span><span class="sxs-lookup"><span data-stu-id="0e356-113">The recipients of the message whose names you want to put on the <strong>To</strong> line in the message.Separate the recipient names that you specify in this argument (and in the <em>Cc</em> and <em>Bcc</em> arguments) with a semicolon (;).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e356-114"><strong>Cc</strong></span><span class="sxs-lookup"><span data-stu-id="0e356-114"><strong>Cc</strong></span></span></p></td>
<td><p><span data-ttu-id="0e356-115">Nein</span><span class="sxs-lookup"><span data-stu-id="0e356-115">No</span></span></p></td>
<td><p><span data-ttu-id="0e356-116">Die Empfänger der Nachricht, deren Namen Sie der CC-Zeile (&quot;Carbon Copy&quot;) in der Nachricht hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="0e356-116">The message recipients whose names you want to put on the Cc (&quot;carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e356-117"><strong>Bcc</strong></span><span class="sxs-lookup"><span data-stu-id="0e356-117"><strong>Bcc</strong></span></span></p></td>
<td><p><span data-ttu-id="0e356-118">Nein</span><span class="sxs-lookup"><span data-stu-id="0e356-118">No</span></span></p></td>
<td><p><span data-ttu-id="0e356-119">Die Empfänger der Nachricht, deren Namen Sie der Bcc-Zeile (&quot;Blind Carbon Copy&quot;) in der Nachricht hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="0e356-119">The message recipients whose names you want to put on the Bcc (&quot;blind carbon copy&quot;) line in the message.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e356-120"><strong>Subject</strong></span><span class="sxs-lookup"><span data-stu-id="0e356-120"><strong>Subject</strong></span></span></p></td>
<td><p><span data-ttu-id="0e356-121">Nein</span><span class="sxs-lookup"><span data-stu-id="0e356-121">No</span></span></p></td>
<td><p><span data-ttu-id="0e356-p101">Der Betreff der Nachricht. Dieser Text wird auf der Zeile <strong>Betreff</strong> der Nachricht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0e356-p101">The subject of the message. This text appears on the <strong>Subject</strong> line in the message.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e356-124"><strong>Body</strong></span><span class="sxs-lookup"><span data-stu-id="0e356-124"><strong>Body</strong></span></span></p></td>
<td><p><span data-ttu-id="0e356-125">Nein</span><span class="sxs-lookup"><span data-stu-id="0e356-125">No</span></span></p></td>
<td><p><span data-ttu-id="0e356-p102">Der Text, den Sie im Haupttext der E-Mail-Nachricht eingeben möchten. Wenn Sie dieses Argument leer lassen, wird kein zusätzlicher Text in der Nachricht eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="0e356-p102">The text that you want to include in the main body of the mail message. If you leave this argument blank, no additional text is included in the message.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="0e356-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e356-128">Remarks</span></span>

<span data-ttu-id="0e356-129">Die **SendenEMail** -Aktion ist nur in den Makroereignissen **[Nach Löschvorgang](after-delete-macro-event.md)**, **[Nach Eingabe](after-insert-macro-event.md)** und **[Nach Aktualisierung](after-update-macro-event.md)** verfügbar.</span><span class="sxs-lookup"><span data-stu-id="0e356-129">The **SendEmail** action is available only in the **[After Delete](after-delete-macro-event.md)**, **[After Insert](after-insert-macro-event.md)**, and **[After Update](after-update-macro-event.md)** macro events.</span></span>

<span data-ttu-id="0e356-130">Mit der **SendenEMail** -Aktion wird die Nachricht nicht zum Bearbeiten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0e356-130">The **SendEmail** action does not display the message for editing.</span></span>

