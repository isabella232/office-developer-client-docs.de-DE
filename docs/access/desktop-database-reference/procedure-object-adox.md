---
title: Procedure-Objekt (ADOX)
TOCTitle: Procedure object (ADOX)
ms:assetid: d5fcf0fe-f59f-e114-dc11-515f11c2a2c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250076(v=office.15)
ms:contentKeyID: 48547972
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ad8f87aa78fbc05694fc53f0d4a55dce43315077
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301393"
---
# <a name="procedure-object-adox"></a>Procedure-Objekt (ADOX)


**Gilt für**: Access 2013, Office 2013

Stellt eine gespeicherte Prozedur dar. Wenn es in Verbindung mit dem ADO-Objekt [Command](command-object-ado.md) verwendet wird, kann das **Procedure** -Objekt zum Hinzufügen, Löschen oder Ändern von gespeicherten Prozeduren verwendet werden.

## <a name="remarks"></a>Bemerkungen

Mit dem **Procedure**-Objekt können Sie eine gespeicherte Prozedur erstellen, ohne die CREATE PROCEDURE-Syntax des Anbieters zu kennen oder zu verwenden.

Die Eigenschaften eines **Procedure** -Objekts ermöglichen Folgendes:

  - Identifizieren der Prozedur, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.

  - Angeben des ADO-Objekts **Command**, das zum Erstellen oder Ausführen der Prozedur verwendet werden kann, indem Sie die [Command](command-property-adox.md)-Eigenschaft verwenden.

  - Zurückgeben von Datumsinformationen, indem Sie die Eigenschaften [DateCreated](datecreated-property-adox.md) und [DateModified](datemodified-property-adox.md) verwenden.

