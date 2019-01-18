---
title: SetDisplayedCategories-Makroaktion
TOCTitle: SetDisplayedCategories macro action
ms:assetid: e8bf39a6-c639-2232-7b21-3b0badf37e4b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836053(v=office.15)
ms:contentKeyID: 48548429
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm20026
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f08b9a8980fc6f08a9f91366d38f65e4365a037e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711420"
---
# <a name="setdisplayedcategories-macro-action"></a>SetDisplayedCategories-Makroaktion


**Betrifft**: Access 2013, Office 2013

Sie können mithilfe der **FestlegenAngezeigteKategorien** -Aktion festlegen, welche Kategorien in der Titelleiste des Navigationsbereichs unter **Navigieren zur Kategorie** angezeigt werden. Wenn Sie beispielsweise verhindern möchten, dass Benutzer den Navigationsbereich wechseln, sodass nach **Erstellt am** sortierte Objekte angezeigt werden, können Sie mit dieser Aktion die Option in der Dropdownliste der Titelleiste ausblenden.

## <a name="setting"></a>Einstellung

Die **FestlegenAngezeigteKategorien** -Aktion hat die folgenden Argumente.

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
<td><p><strong>Show</strong></p></td>
<td><p>Wählen Sie <strong>Ja</strong> aus, um die Kategorien einzublenden, und <strong>Nein</strong>, um sie auszublenden.</p></td>
</tr>
<tr class="even">
<td><p><strong>Category</strong></p></td>
<td><p>Geben Sie den Namen der Kategorie ein, die Sie ein- oder ausblenden möchten, oder wählen Sie ihn aus. Lassen Sie das Feld leer, um alle Kategorien ein- oder auszublenden.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

  - Die Beschriftung in der Titelleiste des Navigationsbereichs gibt an, welcher Filter ggf. derzeit aktiv ist. Klicken Sie auf eine beliebige Stelle in der Leiste, um die Dropdownliste anzuzeigen. Die durch diese Makroaktion gesteuerten Elemente werden unter **Navigieren zur Kategorie** angezeigt.

  - Diese Aktion ist nur aktiviert oder deaktiviert die Anzeige des angegebenen Kategorie oder Kategorien; Wechseln der Anzeige im Navigationsbereich wird nicht ausgeführt. Angenommen, wenn Sie Objekte nach **Erstellungsdatum** sortiert anzeigen, und Sie die **FestlegenAngezeigteKategorien** -Aktion verwenden, um **die Option** zu deaktivieren, wechselt Access im Navigationsbereich zu einer anderen Kategorie nicht.

  - Verwenden Sie die **FestlegenAngezeigteKategorien** -Methode des **DoCmd** -Objekts, um die **FestlegenAngezeigteKategorien** -Aktion in einem VBA-Modul auszuführen.

