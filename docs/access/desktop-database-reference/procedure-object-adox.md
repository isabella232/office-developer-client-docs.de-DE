---
title: Procedure-Objekt (ADOX)
TOCTitle: Procedure object (ADOX)
ms:assetid: d5fcf0fe-f59f-e114-dc11-515f11c2a2c1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250076(v=office.15)
ms:contentKeyID: 48547972
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 11f65742ee1497d32ab6fc79cc11db9b1f9d5d0b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552696"
---
# <a name="procedure-object-adox"></a>Procedure-Objekt (ADOX)


**Gilt für**: Access 2013, Office 2013

Stellt eine gespeicherte Prozedur dar. Wenn es in Verbindung mit dem ADO-Objekt [Command](command-object-ado.md) verwendet wird, kann das **Procedure** -Objekt zum Hinzufügen, Löschen oder Ändern von gespeicherten Prozeduren verwendet werden.

## <a name="remarks"></a>HinwBemerkungeneise

Mit dem **Procedure**-Objekt können Sie eine gespeicherte Prozedur erstellen, ohne die CREATE PROCEDURE-Syntax des Anbieters zu kennen oder zu verwenden.

Die Eigenschaften eines **Procedure** -Objekts ermöglichen Folgendes:

  - Identifizieren der Prozedur, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.

  - Angeben des ADO-Objekts **Command**, das zum Erstellen oder Ausführen der Prozedur verwendet werden kann, indem Sie die [Command](command-property-adox.md)-Eigenschaft verwenden.

  - Zurückgeben von Datumsinformationen, indem Sie die Eigenschaften [DateCreated](datecreated-property-adox.md) und [DateModified](datemodified-property-adox.md) verwenden.

