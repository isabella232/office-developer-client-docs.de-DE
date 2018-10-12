---
title: Ordner
TOCTitle: Folders
ms:assetid: b72b5705-d77a-4cad-873d-457b9fb6553e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff184634(v=office.15)
ms:contentKeyID: 55119856
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: e0fd6aa6ff6a7c4d6c4821858aa8d2a3ca60b2c3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25406428"
---
# <a name="folders"></a>Ordner

In diesem Abschnitt finden Sie Beispielaufgaben im Zusammenhang mit Ordnern. [Folder](https://msdn.microsoft.com/library/bb645774\(v=office.15\))-Objekte stellen die Ordnerhierarchie dar, in der Microsoft Outlook-Elemente gespeichert werden. Beispiele für Ordner sind die Ordner „Kalender“, „E-Mail“ und „Gelöschte Elemente“. In der primären Interopassembly (Primary Interop Assembly, PIA) von Outlook werden Member des **Folder**-Objekts als Member des [MAPIFolde](https://msdn.microsoft.com/library/bb624369\(v=office.15\))-Objekts verfügbar gemacht.

## <a name="in-this-section"></a>Inhalt dieses Abschnitts

|Thema|Beschreibung|
|:----|:----------|
|[Hinzufügen eines Ordners zur Ordnerliste](how-to-add-a-folder-to-the-folder-list.md) |Verwendet die [Add(String, Object)](https://msdn.microsoft.com/library/bb645065\(v=office.15\))-Methode, um einen Ordner zur Ordnerliste von Outlook hinzuzufügen.|
|[Aufzählen von Ordnern](how-to-enumerate-folders.md)  |Listet Ordner durch das Durchlaufen einer Sammlung von Ordnern auf.|
|[Abrufen eines Standardordners und Auflisten seiner Unterordner](how-to-get-a-default-folder-and-enumerate-its-subfolders.md) |Ruft einen Standardordner im Standardspeicher des Benutzers an und listet die Unterordner auf.|
|[Abrufen eines Ordners basierend auf seinem Ordnerpfad](how-to-get-a-folder-based-on-its-folder-path.md)  |Ruft zugehörige Ordner mithilfe eines Ordnerpfads ab.|
|[Auswählen eines Ordners und Anzeigen von Ordnerinformationen](how-to-select-a-folder-and-display-folder-information.md)  |Zeigt Informationen zu einem Ordner programmatisch an, den ein Benutzer aus einer Liste angegebener Ordner auswählt.|
|[Abrufen der Standardnachrichtenklasse eines Ordners](how-to-get-the-default-message-class-of-a-folder.md)  |Verwendet die [DefaultMessageClass](https://msdn.microsoft.com/library/bb646541\(v=office.15\))-Eigenschaft, um die standardmäßige Nachrichtenklasse eines Ordners abzurufen.|
|[Zugreifen auf lösungsspezifische Daten, die als ausgeblendete Nachricht in einem Ordner gespeichert sind](how-to-access-solution-specific-data-stored-as-a-hidden-message-in-a-folder.md)  |Verwendet das [StorageItem](https://msdn.microsoft.com/library/bb623436\(v=office.15\))-Objekt zum Abrufen von Daten, die als ausgeblendete Nachricht einer bestimmten Nachrichtenklasse in einem Ordner gespeichert sind.|
|[Sicherstellen, dass benutzerdefinierte Elementeigenschaften in Abfragen auf Ordnerebene unterstützt werden](how-to-ensure-that-custom-item-properties-are-supported-in-folder-level-queries.md) |Zeigt, wie Sie sicherstellen, dass beim Hinzufügen einer benutzerdefinierten Eigenschaft zu einem Elementtyp die Eigenschaft auch dem Ordner hinzugefügt wird, sodass Sie auf Ordnerebene eine Abfrage nach dieser benutzerdefinierten Eigenschaft ausführen können.|

## <a name="see-also"></a>Siehe auch

- [Calendar](calendar.md)
- [Kontakte](contacts.md)
- [Mail](mail.md)
- [Gewusst wie... (Outlook 2013 PIA-Referenz)](how-do-i-outlook-2013-pia-reference.md)

