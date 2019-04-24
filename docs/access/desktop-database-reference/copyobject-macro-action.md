---
title: CopyObject-Makroaktion
TOCTitle: CopyObject macro action
ms:assetid: 746f61df-d5db-284a-0897-75820c2be11f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195876(v=office.15)
ms:contentKeyID: 48545661
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12836
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2d1fb13d04691b7bf5e0aafcc484cfc4f471e1e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295492"
---
# <a name="copyobject-macro-action"></a>CopyObject-Makroaktion

**Gilt für**: Access 2013, Office 2013

Sie können die **KopierenObjekt** -Aktion verwenden, um das angegebene Datenbankobjekt in eine andere Access-Datenbank oder innerhalb derselben Datenbank oder desselben Access-Projekts unter einem neuen Namen zu kopieren. Sie können ein vorhandenes Objekt beispielsweise in eine andere Datenbank kopieren oder dort sichern oder schnell durch einige Änderungen ein ähnliches Objekt erstellen.

> [!NOTE]
> Diese Aktion ist nicht zulässig, wenn die Datenbank nicht vertrauenswürdig ist. 

## <a name="setting"></a>Einstellung

Die **KopierenObjekt**-Aktion hat die folgenden Argumente.

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
<td><p><strong>Zieldatenbank</strong></p></td>
<td><p>Ein gültiger Pfad und Dateiname für die Zieldatenbank. Geben Sie den Pfad und den Dateinamen im Feld <strong>Zieldatenbank</strong> im Abschnitt <strong>Aktionsargumente</strong> des Bereichs Makro-Generator ein. Lassen Sie dieses Argument leer, wenn Sie die aktuelle Datenbank auswählen möchten.</p><p><strong>Hinweis</strong>: dieses Argument ist nur in der Access-Datenbankumgebung verfügbar. Wenn diese Aktion in einer Access-Projektumgebung (ADP) verwendet wird, muss das Argument Zieldatenbank leer sein.</p>
<p>Wenn Sie ein Makro, das die <strong>KopierenObjekt</strong>-Aktion enthält, in einer Bibliotheksdatenbank ausführen und dieses Argument leer lassen, wird dieses Objekt von Microsoft Office Access 2007 in die Bibliotheksdatenbank kopiert.</p></td>
</tr>
<tr class="even">
<td><p><strong>Neuer Name</strong></p></td>
<td><p>Ein neuer Name für das Objekt. Lassen Sie dieses Argument beim Kopieren in eine andere Datenbank leer, um den Namen beizubehalten.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Objekttyp (Herkunft)</strong></p></td>
<td><p>Der Objekttyp, den Sie kopieren möchten. Klicken Sie auf <strong>Tabelle</strong>, <strong>Abfrage</strong>, <strong>Formular</strong>, <strong>Bericht</strong>, <strong>Makro</strong>, <strong>Modul</strong>, <strong>Datenzugriffsseite</strong>, <strong>Serversicht</strong>, <strong>Diagramm</strong>, <strong>Gespeicherte Prozedur</strong> oder <strong>Funktion</strong>. Lassen Sie dieses Argument leer, um das im Navigationsbereich ausgewählte Objekt zu kopieren.</p></td>
</tr>
<tr class="even">
<td><p><strong>Objektname (Herkunft)</strong></p></td>
<td><p>Der Name des Objekts, das Sie kopieren möchten. In der Datenbank des Typs, der mit dem Argument <strong>Objekttyp (Herkunft)</strong> ausgewählt wurde, werden im Feld <strong>Objektname (Herkunft)</strong> alle Objekte angezeigt. Klicken Sie im Feld <strong>Objektname (Herkunft)</strong> auf das zu kopierende Objekt. Wenn Sie das Argument <strong>Objekttyp (Herkunft)</strong> leer lassen, müssen Sie auch dieses Argument leer lassen. Wenn Sie ein Makro ausführen, das die <strong>KopierenObjekt</strong>-Aktion in einer Bibliotheksdatenbank enthält, sucht Access zunächst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Objekt mit diesem Namen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Bemerkungen

Sie müssen für diese Aktion für mindestens eines der Argumente **Zieldatenbank** und **Neuer Name** einen Wert eingeben.

If you leave the **Source Object Type** and **Source Object Name** arguments blank, Access copies the object selected in the Navigation Pane. To select an object in the Navigation Pane, you can use the **SelectObject** action with the In Navigation Pane argument set to **Yes**.

Die **KopierenObjekt** -Aktion ist mit dem manuellen Ausführen der folgenden Schritte vergleichbar:

1. Wählen Sie ein Objekt im Navigationsbereich aus.

2. Klicken Sie auf der Registerkarte Home in der Gruppe Clipboard auf Copy.

3. Klicken Sie auf derselben Registerkarte auf **Einfügen**.Das Dialogfeld **Einfügen als** wird angezeigt, damit Sie dem Objekt einen neuen Namen zuweisen können. Diese Schritte werden von der **KopierenObjekt** -Aktion automatisch ausgeführt.

> [!NOTE]
> [!HINWEIS] Beim Kopieren von Datenzugriffsseiten kopiert die **KopierenObjekt** -Aktion nur die Verknüpfung zur zugeordneten HTM-Datei und nicht die Datei selbst.

Der Pfad und der Dateiname der Zieldatenbank müssen vorhanden sein, bevor das Makro die **KopierenObjekt** -Aktion ausführt. Wenn sie nicht vorhanden sind, zeigt Access eine Fehlermeldung an.

Verwenden Sie die **CopyObject** -Methode des **DoCmd** -Objekts, um die **KopierenObjekt** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

Sie können ein Objekt, das im Navigationsbereich ausgewählt wurde, oder ein derzeit geöffnetes Objekt auch manuell kopieren, indem Sie auf die Registerkarte **Datei** und dann auf **Speichern unter** klicken. Dieser Befehl erstellt nur in der aktuellen Datenbank eine Kopie des Objekts. Geben Sie im Dialogfeld **Speichern unter** den Namen für die Kopie ein, und wählen Sie den zu speichernden Objekttyp aus. Falls das ursprüngliche Objekt bereits gespeichert wurde und Sie es in der aktuellen Datenbank unter einem neuen Namen speichern, bleibt die ursprüngliche Version mit dem alten Namen weiterhin vorhanden.

So kopieren Sie ein Objekt manuell in eine andere Access-Datenbank:

1. Klicken Sie auf der Registerkarte **Externe Daten** in der Gruppe **Exportieren** auf **Mehr**, und klicken Sie dann auf **Access-Datenbank**.

2. Geben Sie im Dialogfeld **Exportieren - Access-Datenbank** den Dateinamen der Zieldatenbank ein.-oder-Klicken Sie auf **Durchsuchen**, um das Dialogfeld **Datei speichern** anzuzeigen, suchen Sie die Zieldatenbank, und klicken Sie dann auf **Speichern**.

3. Klicken Sie im Dialogfeld **Exportieren - Access-Datenbank** auf **OK**. Das Dialogfeld **Exportieren** wird angezeigt.

4. Geben Sie im Dialogfeld **Exportieren** einen Namen für das Objekt in der Zieldatenbank ein. Wählen Sie eine beliebige anwendbare Option für Tabellen aus, z. B. **Definitionen und Daten exportieren** oder **Nur Definitionen**. Klicken Sie auf **OK**, wenn Sie den Vorgang abgeschlossen haben.

