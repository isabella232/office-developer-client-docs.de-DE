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
ms.localizationpriority: medium
ms.openlocfilehash: 5334c23603fbc90dc3736236a60dd256bc50c11c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602101"
---
# <a name="opendiagram-macro-action"></a>OpenDiagram-Makroaktion

**Gilt für**: Access 2013, Office 2013

In einem Access-Projekt können Sie die **ÖffnenDiagramm** -Aktion verwenden, um ein Datenbankdiagramm in der Entwurfsansicht zu öffnen.

> [!NOTE]
> Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **ÖffnenDiagramm**-Aktion verwendet das folgende Argument.

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
<td><p>Der Name des zu öffnenden Datenbankdiagramms. Im Feld <strong>"Diagrammname"</strong> im Abschnitt <strong>"Aktionsargumente"</strong> im Bereich "Makro-Generator" werden alle Datenbankdiagramme in der aktuellen Datenbank angezeigt. Dies ist ein erforderliches Argument. Wenn Sie ein Makro, das die <strong>ÖffnenDiagramm</strong>-Aktion enthält, in einer Bibliotheksdatenbank ausführen, sucht Microsoft Access zuerst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Diagramm mit diesem Namen.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>HinwBemerkungeneise

Diese Aktion entspricht dem Doppelklicken auf ein Datenbankdiagramm im Navigationsbereich oder dem Klicken mit der rechten Maustaste auf das Datenbankdiagramm im Navigationsbereich und dem anschließenden Klicken auf **Entwurfsansicht**.

> [!TIP]
> [!TIPP] Sie können ein Datenbankdiagramm aus dem Navigationsbereich in eine Makro aktionszeile ziehen. Hierdurch wird automatisch eine **ÖffnenDiagramm** -Aktion erstellt, die das Datenbankdiagramm in der Entwurfsansicht öffnet.

Verwenden Sie die **OpenDiagram** -Methode des **DoCmd** -Objekts, um die **ÖffnenDiagramm** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

