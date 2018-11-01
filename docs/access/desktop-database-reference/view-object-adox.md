---
title: View-Objekt (ADOX - Access-desktop-Datenbank (engl.))
TOCTitle: View Object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6e1c3b2cc99cad4ba3b9ee71f0c44ee67b32d41d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873131"
---
# <a name="view-object-adox"></a>View-Objekt (ADOX)


**Betrifft**: Access 2013, Office 2013

Stellt eine gefilterte Datensatzgruppe oder eine virtuelle Tabelle dar. Wenn es in Verbindung mit dem ADO-Objekt [Command](command-object-ado.md) verwendet wird, kann das **View** -Objekt zum Hinzufügen, Löschen oder Ändern von Sichten verwendet werden.

## <a name="remarks"></a>Hinweise

Eine Sicht ist eine virtuelle Tabelle, die aus anderen Datenbanktabellen oder -sichten erstellt wird. Mit dem **View** -Objekt können Sie eine Sicht erstellen, ohne die CREATE VIEW-Syntax des Anbieters zu kennen oder zu verwenden.

Die Eigenschaften eines **View** -Objekts ermöglichen Folgendes:

  - Identifizieren der Sicht, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.

  - Angeben des ADO-Objekts **Command**, das zum Hinzufügen, Löschen oder Ändern von Sichten verwendet werden kann, indem Sie die [Command](command-property-adox.md)-Eigenschaft verwenden.

  - Zurückgeben von Datumsinformationen, indem Sie die Eigenschaften [DateCreated](datecreated-property-adox.md) und [DateModified](datemodified-property-adox.md) verwenden.

