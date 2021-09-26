---
title: GoToPage-Makroaktion
TOCTitle: GoToPage macro action
ms:assetid: 611aadff-83b7-e74d-4093-93fb5ce6e3ab
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194858(v=office.15)
ms:contentKeyID: 48545199
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm129285
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 9e4d7acd7c0f07f4d18a0a997c999cb877dbcb45
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626498"
---
# <a name="gotopage-macro-action"></a>GoToPage-Makroaktion

**Gilt für**: Access 2013, Office 2013

Mit der **GeheZuSeite** -Aktion können Sie den Fokus im aktiven Formular auf das erste Steuerelement auf einer angegebenen Seite verschieben. Sie können diese Aktion verwenden, wenn Sie ein Formular mit Seitenumbrüchen erstellt haben, das Gruppen verwandter Informationen enthält. Sie könnten Sie z. B. ein Mitarbeiterformular verwenden, das persönliche Informationen auf der einen Seite, firmenbezogene Informationen auf einer weiteren Seite und Umsatzinformationen auf einer dritten Seite enthält. Mit der **GeheZuSeite** -Aktion können Sie den Fokus auf die gewünschte Seite verschieben. Sie können auch Registersteuerelemente verwenden, um mehrere Seiten mit Informationen auf einem einzigen Formular darzustellen.

## <a name="setting"></a>Einstellung

Die **GeheZuSeite**-Aktion verwendet die folgenden Argumente.

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
<td><p><strong>Seitenzahl</strong></p></td>
<td><p>Die Nummer der Seite, auf die Sie den Fokus verschieben möchten. Geben Sie die Seitenzahl im Feld <strong>"Seitenzahl"</strong> im Abschnitt <strong>"Aktionsargumente"</strong> im Bereich "Makro-Generator" ein. Wenn Sie dieses Argument nicht angeben, bleibt der Fokus auf der aktuellen Seite. Sie können die Argumente <strong>"Rechts"</strong> und <strong>"Unten"</strong> verwenden, um den Teil der Seite anzuzeigen, der angezeigt werden soll.</p></td>
</tr>
<tr class="even">
<td><p><strong>Right</strong></p></td>
<td><p>Die horizontale Ausrichtung der Stelle auf der Seite, gemessen vom linken Rand des umgebenden Fensters, die am linken Rand des Fensters angezeigt werden soll. Dieses Argument ist erforderlich, wenn Sie das Argument <strong>Abwärts</strong> angeben.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Down</strong></p></td>
<td><p>Die vertikale Ausrichtung der Stelle auf der Seite, gemessen vom oberen Rand des umgebenden Fensters, die am oberen Rand des Fensters angezeigt werden soll. Dieses Argument ist erforderlich, wenn Sie das Argument <strong>Rechts</strong> angeben.</p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> Die Argumente **Rechts** und **Abwärts** werden, abhängig von den regionalen Einstellungen in der Windows-Systemsteuerung, in Zoll oder Zentimetern gemessen.

## <a name="remarks"></a>Bemerkungen

Sie können diese Aktion verwenden, um das erste Steuerelement (gemäß Definition in der Aktivierreihenfolge des Formulars) auf der angegebenen Seite auszuwählen. Verwenden Sie die **GeheZuSteuerelement**-Aktion, um den Fokus auf ein bestimmtes Steuerelement im Formular zu verschieben.

Sie können die Argumente **"Rechts"** und **"Unten"** für Formulare verwenden, deren Seiten größer als das Access-Fenster sind. Verwenden Sie das Argument **Seitenzahl**, um sich zur gewünschten Seite zu bewegen, und verwenden Sie dann die Argumente **Rechts** und **Abwärts**, um den gewünschten Teil der Seite anzuzeigen. Access zeigt den Teil der Seite an, dessen obere linke Ecke den angegebenen Abstand von der linken oberen Ecke der Seite hat.

In den folgenden Fällen können Sie die **GeheZuSeite** -Aktion nicht verwenden:

- Setzen des Fokus auf eine Seite eines ausgeblendeten Formulars.

- Verschieben des Fokus von einer Seite zu einer anderen innerhalb des Registersteuerelements.

Verwenden Sie die **GoToPage** -Methode des **DoCmd** -Objekts, um die **GeheZuSeite** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

