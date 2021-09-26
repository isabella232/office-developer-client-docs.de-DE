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
ms.localizationpriority: medium
ms.openlocfilehash: 16467b8b471111a7210678526e3230726ce5447d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621857"
---
# <a name="setdisplayedcategories-macro-action"></a>SetDisplayedCategories-Makroaktion


**Gilt für**: Access 2013, Office 2013

Sie können mithilfe der **FestlegenAngezeigteKategorien** -Aktion festlegen, welche Kategorien in der Titelleiste des Navigationsbereichs unter **Navigieren zur Kategorie** angezeigt werden. Wenn Sie beispielsweise verhindern möchten, dass Benutzer den Navigationsbereich wechseln, sodass nach **Erstellt am** sortierte Objekte angezeigt werden, können Sie mit dieser Aktion die Option in der Dropdownliste der Titelleiste ausblenden.

## <a name="setting"></a>Einstellung

Die **FestlegenAngezeigteKategorien**-Aktion hat die folgenden Argumente.

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
<td><p><strong>Kategorie</strong></p></td>
<td><p>Geben Sie den Namen der Kategorie ein, die Sie ein- oder ausblenden möchten, oder wählen Sie ihn aus. Lassen Sie das Feld leer, um alle Kategorien ein- oder auszublenden.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

  - Die Beschriftung in der Titelleiste des Navigationsbereichs gibt an, welcher Filter ggf. derzeit aktiv ist. Klicken Sie auf eine beliebige Stelle in der Leiste, um die Dropdownliste anzuzeigen. Die durch diese Makroaktion gesteuerten Elemente werden unter **Navigieren zur Kategorie** angezeigt.

  - This action only enables or disables the display of the specified category or categories; it does not perform any switching of the Navigation Pane display. For example, if you are displaying objects sorted by **Creation Date** and you use the **SetDisplayedCategories** action to disable the **Creation Date** option, Access does not switch the Navigation Pane to another category.

  - Verwenden Sie die **FestlegenAngezeigteKategorien**-Methode des **DoCmd**-Objekts, um die **FestlegenAngezeigteKategorien**-Aktion in einem VBA-Modul auszuführen.

