---
title: KopierenObjekt-Makroaktion
TOCTitle: CopyObject Macro Action
ms:assetid: 746f61df-d5db-284a-0897-75820c2be11f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195876(v=office.15)
ms:contentKeyID: 48545661
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12836
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 09edfd37edb5a0cb237bd94f7f13449690cf18bb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868224"
---
# <a name="copyobject-macro-action"></a>KopierenObjekt-Makroaktion


**Betrifft**: Access 2013, Office 2013

Sie können die **KopierenObjekt** -Aktion verwenden, um das angegebene Datenbankobjekt in eine andere Access-Datenbank oder innerhalb derselben Datenbank oder desselben Access-Projekts unter einem neuen Namen zu kopieren. Sie können ein vorhandenes Objekt beispielsweise in eine andere Datenbank kopieren oder dort sichern oder schnell durch einige Änderungen ein ähnliches Objekt erstellen.


> [!NOTE]
> [!HINWEIS] Diese Aktion wird nicht erlaubt, wenn die Datenbank nicht vertrauenswürdig ist. Informationen zur Aktivierung von Makros finden Sie unter den Links im Abschnitt See Also dieses Artikels.



## <a name="setting"></a>Einstellung

Die **KopierenObjekt** -Aktion hat die folgenden Argumente.

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
<td><p>Ein gültiger Pfad und Dateiname für die Zieldatenbank. Geben Sie den Pfad und den Dateinamen im Feld Zieldatenbank im Abschnitt Aktionsargumente des Bereichs Makro-Generator ein. Lassen Sie dieses Argument leer, wenn die aktuelle Datenbank ausgewählt werden soll. 

</p>

> [!NOTE]
> Dieses Argument ist nur in der Access-Datenbankumgebung verfügbar. Wenn diese Aktion in einer Access-Projektumgebung (ADP) verwendet wird, muss das Argument Zieldatenbank leer sein.


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
<td><p>Der Name des zu kopierenden Objekts. Das Feld <strong>Objektname Quelle</strong> zeigt alle Objekte in der Datenbank an, die durch das Argument <strong>Objekttyp Quelle</strong> . Klicken Sie im Feld <strong>Objektname Quelle</strong> auf das zu kopierende Objekt. Lassen Sie dieses Argument leer, wenn Sie das Argument <strong>Objekttyp Quelle</strong> leer lassen. Wenn Sie ein Makro ausführen, das die <strong>KopierenObjekt</strong>-Aktion in einer Bibliotheksdatenbank enthält, sucht Access zunächst in der Bibliotheksdatenbank und dann in der aktuellen Datenbank nach dem Objekt mit diesem Namen.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Hinweise

Sie müssen für diese Aktion für mindestens eines der Argumente **Zieldatenbank** und **Neuer Name** einen Wert eingeben.

Wenn Sie die Argumente Objekttyp (Herkunft) und Objektname (Herkunft) leer lassen, wird das im Navigationsbereich ausgewählte Objekt von Access kopiert. Zum Auswählen eines Objekts im Navigationsbereich können Sie die AuswählenObjekt-Aktion verwenden, wobei das Argument Im Navigationsbereich auf Ja festgelegt sein muss.

Die **KopierenObjekt** -Aktion ist mit dem manuellen Ausführen der folgenden Schritte vergleichbar:

1.  Wählen Sie ein Objekt im Navigationsbereich aus.

2.  Klicken Sie auf der Registerkarte Home in der Gruppe Clipboard auf Copy.

3.  Klicken Sie auf derselben Registerkarte auf **Einfügen**.Das Dialogfeld **Einfügen als** wird angezeigt, damit Sie dem Objekt einen neuen Namen zuweisen können. Diese Schritte werden von der **KopierenObjekt** -Aktion automatisch ausgeführt.


> [!NOTE]
> [!HINWEIS] Beim Kopieren von Datenzugriffsseiten kopiert die **KopierenObjekt** -Aktion nur die Verknüpfung zur zugeordneten HTM-Datei und nicht die Datei selbst.



Der Pfad und der Dateiname der Zieldatenbank müssen vorhanden sein, bevor das Makro die **KopierenObjekt** -Aktion ausführt. Wenn sie nicht vorhanden sind, zeigt Access eine Fehlermeldung an.

Verwenden Sie die **CopyObject** -Methode des **DoCmd** -Objekts, um die **KopierenObjekt** -Aktion in einem VBA-Modul (Visual Basic für Applikationen) auszuführen.

Sie können ein Objekt, das im Navigationsbereich ausgewählt wurde, oder ein derzeit geöffnetes Objekt auch manuell kopieren, indem Sie auf die Registerkarte **Datei** und dann auf **Speichern unter** klicken. Dieser Befehl erstellt nur in der aktuellen Datenbank eine Kopie des Objekts. Geben Sie im Dialogfeld **Speichern unter** den Namen für die Kopie ein, und wählen Sie den zu speichernden Objekttyp aus. Falls das ursprüngliche Objekt bereits gespeichert wurde und Sie es in der aktuellen Datenbank unter einem neuen Namen speichern, bleibt die ursprüngliche Version mit dem alten Namen weiterhin vorhanden.

So kopieren Sie ein Objekt manuell in eine andere Access-Datenbank:

1.  Klicken Sie auf der Registerkarte **Externe Daten** in der Gruppe **Exportieren** auf **Mehr**, und klicken Sie dann auf **Access-Datenbank**.

2.  Geben Sie im Dialogfeld **Exportieren - Access-Datenbank** den Dateinamen der Zieldatenbank ein.-oder-Klicken Sie auf **Durchsuchen**, um das Dialogfeld **Datei speichern** anzuzeigen, suchen Sie die Zieldatenbank, und klicken Sie dann auf **Speichern**.

3.  Klicken Sie im Dialogfeld **Exportieren - Access-Datenbank** auf **OK**. Das Dialogfeld **Exportieren** wird angezeigt.

4.  Geben Sie im Dialogfeld **Exportieren** einen Namen für das Objekt in der Zieldatenbank ein. Wählen Sie eine beliebige anwendbare Option für Tabellen aus, z. B. **Definitionen und Daten exportieren** oder **Nur Definitionen**. Klicken Sie auf **OK**, wenn Sie den Vorgang abgeschlossen haben.

