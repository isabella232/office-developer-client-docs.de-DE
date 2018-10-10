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
# <a name="customization-file-logs-section"></a>Logs-Abschnitt der Anpassungsdatei

**Betrifft**: Access 2013 | Office 2013

Der **logs** -Abschnitt enthält einen Protokolldateieintrag, durch den der Name einer Datei angegeben wird, in der Fehler während der Operation des **DataFactory** -Objekts aufgezeichnet werden.

## <a name="syntax"></a>Syntax

Ein Protokolldateieintrag hat folgendes Format:

`err=FileName`

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>err</strong></p></td>
<td><p>Eine literale Zeichenfolge, durch die angegeben wird, dass es sich um einen Protokolldateieintrag handelt.</p></td>
</tr>
<tr class="even">
<td><p><em>FileName</em></p></td>
<td><p>Einen vollständigen Pfad und Dateinamen. Der typische Dateiname lautet <strong>C:\msdfmap.log</strong>.</p></td>
</tr>
</tbody>
</table>


Die Protokolldatei enthält den Benutzernamen, HRESULT, das Datum und die Uhrzeit jedes Fehlers.

