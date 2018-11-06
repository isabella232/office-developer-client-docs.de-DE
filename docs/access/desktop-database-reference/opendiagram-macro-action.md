---
title: OpenDiagram-Makroaktion
TOCTitle: OpenDiagram macro action
ms:assetid: 408e7224-02bb-335a-b1b9-cbccbf6e36ec
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192875(v=office.15)
ms:contentKeyID: 48544427
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm154095
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b04870a416874e2136e21b40c62d8e64a6182efe
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998546"
---
# <a name="opendiagram-macro-action"></a>OpenDiagram-Makroaktion

**Betrifft**: Access 2013, Office 2013

In einem Access-Projekt können Sie die **ÖffnenDiagramm** -Aktion verwenden, um ein Datenbankdiagramm in der Entwurfsansicht zu öffnen.

> [!NOTE]
> [!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **ÖffnenDiagramm** -Aktion verwendet das folgende Argument.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Aktionsargument</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Diagrammname</strong></p></td>
<td><p>Der Name der zu öffnenden Datenbankdiagramms. Feld <strong>Diagrammname</strong> im Abschnitt <strong>Aktionsargument</strong> des Makro-Generators zeigt alle Datenbankdiagramme in der aktuellen Datenbank. Dies ist ein erforderliches Argument. Wenn Sie ein Makro, das die <strong>ÖffnenDiagramm</strong>-Aktion enthält, in einer Bibliotheksdatenbank ausführen, sucht Microsoft Access zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Diagramm mit diesem Namen.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Hinweise

Diese Aktion entspricht dem Doppelklicken auf ein Datenbankdiagramm im Navigationsbereich oder dem Klicken mit der rechten Maustaste auf das Datenbankdiagramm im Navigationsbereich und dem anschließenden Klicken auf **Entwurfsansicht**.

> [!TIP]
> [!TIPP] Sie können ein Datenbankdiagramm aus dem Navigationsbereich in eine Makro aktionszeile ziehen. Hierdurch wird automatisch eine **ÖffnenDiagramm** -Aktion erstellt, die das Datenbankdiagramm in der Entwurfsansicht öffnet.

Verwenden Sie die **OpenDiagram** -Methode des **DoCmd** -Objekts, um die **ÖffnenDiagramm** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

