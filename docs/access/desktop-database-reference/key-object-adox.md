---
title: Key-Objekt (ADOX – Access-Desktopdatenbankreferenz)
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2c230b6ae88cbdfe1e39e4d2c19ad1a64a86283b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59626358"
---
# <a name="key-object-adox"></a>Key-Objekt (ADOX)


**Gilt für**: Access 2013, Office 2013

Stellt ein Primärschlüsselfeld, ein Fremdschlüsselfeld oder ein Feld für einen eindeutigen Schlüssel aus einer Datenbanktabelle dar.

## <a name="remarks"></a>Bemerkungen

Mit dem folgenden Code wird ein neues **Key**-Objekt erstellt:

`Dim obj As New Key`

Die Eigenschaften und Auflistungen eines **Key** -Objekts ermöglichen Folgendes:

- Identifizieren des Schlüssels, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.

- Bestimmen, ob es sich um einen Primär- oder Fremdschlüssel oder um einen eindeutigen Schlüssel handelt, indem Sie die [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox)-Eigenschaft verwenden.

- Zugreifen auf die Datenbankspalten des Schlüssels, indem Sie die [Columns](columns-collection-adox.md)-Auflistung verwenden.

- Angeben des Namens der verwandten Tabelle, indem Sie die [RelatedTable](relatedtable-property-adox.md)-Eigenschaft verwenden.

- Bestimmen der Aktion, die beim Löschen oder Aktualisieren des Primärschlüssels ausgeführt wird, indem Sie die Eigenschaften [DeleteRule](deleterule-property-adox.md) und [UpdateRule](updaterule-property-adox.md) verwenden.

