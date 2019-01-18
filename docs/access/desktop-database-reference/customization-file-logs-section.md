---
title: Anpassungsdatei – Protokollabschnitt
TOCTitle: Customization File Logs section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a9af5d09a7a7a7a7ec97d757d502efbf2402900
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715634"
---
# <a name="customization-file-logs-section"></a><span data-ttu-id="a3d05-102">Anpassungsdatei – Protokollabschnitt</span><span class="sxs-lookup"><span data-stu-id="a3d05-102">Customization File Logs section</span></span>

<span data-ttu-id="a3d05-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a3d05-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a3d05-104">Der **logs** -Abschnitt enthält einen Protokolldateieintrag, durch den der Name einer Datei angegeben wird, in der Fehler während der Operation des **DataFactory** -Objekts aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="a3d05-104">The **logs** section contains a log file entry, which specifies the name of a file that records errors during the operation of the **DataFactory**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3d05-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3d05-105">Syntax</span></span>

<span data-ttu-id="a3d05-106">Ein Protokolldateieintrag hat folgendes Format:</span><span class="sxs-lookup"><span data-stu-id="a3d05-106">A log file entry is of the form:</span></span>

`err=FileName`

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a3d05-107">Argument</span><span class="sxs-lookup"><span data-stu-id="a3d05-107">Part</span></span></p></th>
<th><p><span data-ttu-id="a3d05-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3d05-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a3d05-109"><strong>err</strong></span><span class="sxs-lookup"><span data-stu-id="a3d05-109"><strong>err</strong></span></span></p></td>
<td><p><span data-ttu-id="a3d05-110">Eine literale Zeichenfolge, durch die angegeben wird, dass es sich um einen Protokolldateieintrag handelt.</span><span class="sxs-lookup"><span data-stu-id="a3d05-110">A literal string that indicates this is a log file entry.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a3d05-111"><em>FileName</em></span><span class="sxs-lookup"><span data-stu-id="a3d05-111"><em>FileName</em></span></span></p></td>
<td><p><span data-ttu-id="a3d05-p101">Einen vollständigen Pfad und Dateinamen. Der typische Dateiname lautet <strong>C:\msdfmap.log</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3d05-p101">A complete path and file name. The typical file name is <strong>c:\msdfmap.log</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a3d05-114">Die Protokolldatei enthält den Benutzernamen, HRESULT, das Datum und die Uhrzeit jedes Fehlers.</span><span class="sxs-lookup"><span data-stu-id="a3d05-114">The log file will contain the user name, HRESULT, date, and time of each error.</span></span>

