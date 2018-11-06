---
title: PrintOut-Makroaktion
TOCTitle: PrintOut macro action
ms:assetid: 13688158-1cf1-4b2e-d90a-271c8890e413
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845432(v=office.15)
ms:contentKeyID: 48543368
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm1697
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c2e5b3e2cdfb743df8a098d3978ccd3d6eb66d90
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25999029"
---
# <a name="printout-macro-action"></a>PrintOut-Makroaktion

**Betrifft**: Access 2013, Office 2013

Zum Drucken des aktiven Objekts in der geöffneten Datenbank können Sie die **Drucken** -Aktion verwenden. Sie können Datenblätter, Berichte, Formulare, Datenzugriffsseiten und Module drucken.

> [!NOTE]
> [!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **Drucken** -Aktion hat die folgenden Argumente.

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
<td><p><strong>Druckbereich</strong></p></td>
<td><p>Der zu druckende Bereich. Klicken Sie im Feld Druckbereich im Abschnitt Aktionsargumente des Bereichs Makro-Generator auf Alle (der Benutzer kann alle Objekte drucken), auf Markierung (der Benutzer kann den Teil des Objekts drucken, der markiert ist) oder auf Seite (der Benutzer kann einen Seitenbereich mit den Argumenten Von und Bis angeben). Die Standardeinstellung ist Alle.</p></td>
</tr>
<tr class="even">
<td><p><strong>Von</strong></p></td>
<td><p>Die erste zu druckende Seite. Der Druckvorgang wird am Anfang dieser Seite gestartet. Dieses Argument ist erforderlich, wenn Sie im Feld <strong>Druckbereich</strong> die Option <strong>Seiten</strong> auswählen.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Bis</strong></p></td>
<td><p>Die letzte zu druckende Seite. Der Druckvorgang wird unten auf dieser Seite beendet. Dieses Argument ist erforderlich, wenn Sie im Feld <strong>Druckbereich</strong> die Option <strong>Seiten</strong> auswählen.</p></td>
</tr>
<tr class="even">
<td><p><strong>Druckqualität</strong></p></td>
<td><p>Die Qualität des Ausdrucks. Klicken Sie auf <strong>Hoch</strong>, <strong>Mittel</strong>, <strong>Niedrig</strong> oder <strong>Entwurf</strong>. Je niedriger die Qualität, desto schneller wird das Objekt gedruckt. Die Standardeinstellung ist <strong>Hoch</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Copies</strong></p></td>
<td><p>Die Anzahl der zu druckenden Exemplare. Die Standardeinstellung ist 1.</p></td>
</tr>
<tr class="even">
<td><p><strong>Exemplare sortieren</strong></p></td>
<td><p>Klicken Sie auf <strong>Ja</strong> (gedruckte Exemplare sortieren) oder <strong>Nein</strong> (Exemplare nicht sortieren). Das Objekt wird möglicherweise schneller gedruckt, wenn dieses Argument auf <strong>Nein</strong> festgelegt wird. Die Standardeinstellung ist <strong>Ja</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Diese Aktion ist mit dem Auswählen eines Objekts, dem Klicken auf die Registerkarte **Datei** und dann dem Klicken auf **Drucken** vergleichbar. Mit dieser Aktion wird jedoch kein Dialogfeld **Drucken** angezeigt.

> [!TIP]
> [!TIPP] Erstellen Sie ein Makro mit einer **Drucken** -Aktion mit diesen Einstellungen in den Argumenten, wenn Sie bestimmte Druckeinstellungen häufig verwenden.

Die Argumente für diese Aktion entsprechen den Optionen im Dialogfeld **Drucken**. Im Gegensatz zur **SuchenDatensatz** -Aktion und dem Dialogfeld **Suchen und Ersetzen** werden die Argumenteinstellungen nicht mit den Optionen des Dialogfelds **Drucken** gemeinsam verwendet.

Verwenden Sie die **PrintOut** -Methode des **DoCmd** -Objekts, um die **Drucken** -Aktion in einem Modul für Visual Basic für Applikationen (VBA) auszuführen.

