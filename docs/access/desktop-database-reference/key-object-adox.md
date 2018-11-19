---
title: Key-Objekt (ADOX - Access-desktop-Datenbank (engl.))
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7722130c76516eaa7dcaf0598a5e1c040e21ba25
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025945"
---
# <a name="key-object-adox"></a>Key-Objekt (ADOX)


**Betrifft**: Access 2013, Office 2013

Stellt ein Primärschlüsselfeld, ein Fremdschlüsselfeld oder ein Feld für einen eindeutigen Schlüssel aus einer Datenbanktabelle dar.

## <a name="remarks"></a>Hinweise

Mit dem folgenden Code wird ein neues **Key** -Objekt erstellt:

`Dim obj As New Key`

Die Eigenschaften und Auflistungen eines **Key** -Objekts ermöglichen Folgendes:

- Identifizieren des Schlüssels, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.

- Bestimmen, ob es sich um einen Primär- oder Fremdschlüssel oder um einen eindeutigen Schlüssel handelt, indem Sie die [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox)-Eigenschaft verwenden.

- Zugreifen auf die Datenbankspalten des Schlüssels, indem Sie die [Columns](columns-collection-adox.md)-Auflistung verwenden.

- Angeben des Namens der verwandten Tabelle, indem Sie die [RelatedTable](relatedtable-property-adox.md)-Eigenschaft verwenden.

- Bestimmen der Aktion, die beim Löschen oder Aktualisieren des Primärschlüssels ausgeführt wird, indem Sie die Eigenschaften [DeleteRule](deleterule-property-adox.md) und [UpdateRule](updaterule-property-adox.md) verwenden.

