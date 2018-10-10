---
title: Logs-Abschnitt der Anpassungsdatei
TOCTitle: Customization File Logs Section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 479bac0c61718f12af8fcb1b176b91d3fc57841b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475430"
---
# <a name="customization-file-logs-section"></a><span data-ttu-id="8beee-102">Logs-Abschnitt der Anpassungsdatei</span><span class="sxs-lookup"><span data-stu-id="8beee-102">Customization File Logs Section</span></span>

<span data-ttu-id="8beee-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="8beee-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="8beee-104">Der **logs** -Abschnitt enthält einen Protokolldateieintrag, durch den der Name einer Datei angegeben wird, in der Fehler während der Operation des **DataFactory** -Objekts aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="8beee-104">The **logs** section contains a log file entry, which specifies the name of a file that records errors during the operation of the **DataFactory**.</span></span>

## <a name="syntax"></a><span data-ttu-id="8beee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8beee-105">Syntax</span></span>

<span data-ttu-id="8beee-106">Ein Protokolldateieintrag hat folgendes Format:</span><span class="sxs-lookup"><span data-stu-id="8beee-106">A log file entry is of the form:</span></span>

`err=FileName`

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8beee-107">Argument</span><span class="sxs-lookup"><span data-stu-id="8beee-107">Part</span></span></p></th>
<th><p><span data-ttu-id="8beee-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8beee-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8beee-109"><strong>err</strong></span><span class="sxs-lookup"><span data-stu-id="8beee-109"><strong>err</strong></span></span></p></td>
<td><p><span data-ttu-id="8beee-110">Eine literale Zeichenfolge, durch die angegeben wird, dass es sich um einen Protokolldateieintrag handelt.</span><span class="sxs-lookup"><span data-stu-id="8beee-110">A literal string that indicates this is a log file entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8beee-111"><em>FileName</em></span><span class="sxs-lookup"><span data-stu-id="8beee-111"><em>FileName</em></span></span></p></td>
<td><p><span data-ttu-id="8beee-p101">Einen vollständigen Pfad und Dateinamen. Der typische Dateiname lautet <strong>C:\msdfmap.log</strong>.</span><span class="sxs-lookup"><span data-stu-id="8beee-p101">A complete path and file name. The typical file name is <strong>c:\msdfmap.log</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8beee-114">Die Protokolldatei enthält den Benutzernamen, HRESULT, das Datum und die Uhrzeit jedes Fehlers.</span><span class="sxs-lookup"><span data-stu-id="8beee-114">The log file will contain the user name, HRESULT, date, and time of each error.</span></span>

