---
title: Key-Objekt (ADOX - Access-desktop-Datenbank (engl.))
TOCTitle: Key object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f56a90b7accd1b64c9a52e0a7cf5385f83fd10d5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717139"
---
# <a name="key-object-adox"></a><span data-ttu-id="d003c-102">Key-Objekt (ADOX)</span><span class="sxs-lookup"><span data-stu-id="d003c-102">Key object (ADOX)</span></span>


<span data-ttu-id="d003c-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d003c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d003c-104">Stellt ein Primärschlüsselfeld, ein Fremdschlüsselfeld oder ein Feld für einen eindeutigen Schlüssel aus einer Datenbanktabelle dar.</span><span class="sxs-lookup"><span data-stu-id="d003c-104">Represents a primary, foreign, or unique key field from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="d003c-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d003c-105">Remarks</span></span>

<span data-ttu-id="d003c-106">Mit dem folgenden Code wird ein neues **Key** -Objekt erstellt:</span><span class="sxs-lookup"><span data-stu-id="d003c-106">The following code creates a new **Key**:</span></span>

`Dim obj As New Key`

<span data-ttu-id="d003c-107">Die Eigenschaften und Auflistungen eines **Key** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d003c-107">With the properties and collections of a **Key** object, you can:</span></span>

- <span data-ttu-id="d003c-108">Identifizieren des Schlüssels, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="d003c-108">Identify the key with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="d003c-109">Bestimmen, ob es sich um einen Primär- oder Fremdschlüssel oder um einen eindeutigen Schlüssel handelt, indem Sie die [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="d003c-109">Determine whether the key is primary, foreign, or unique with the [Type](https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/type-property-keyadox) property.</span></span>

- <span data-ttu-id="d003c-110">Zugreifen auf die Datenbankspalten des Schlüssels, indem Sie die [Columns](columns-collection-adox.md)-Auflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="d003c-110">Access the database columns of the key with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="d003c-111">Angeben des Namens der verwandten Tabelle, indem Sie die [RelatedTable](relatedtable-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="d003c-111">Specify the name of the related table with the [RelatedTable](relatedtable-property-adox.md) property.</span></span>

- <span data-ttu-id="d003c-112">Bestimmen der Aktion, die beim Löschen oder Aktualisieren des Primärschlüssels ausgeführt wird, indem Sie die Eigenschaften [DeleteRule](deleterule-property-adox.md) und [UpdateRule](updaterule-property-adox.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="d003c-112">Determine the action performed on deletion or update of a primary key with the [DeleteRule](deleterule-property-adox.md) and [UpdateRule](updaterule-property-adox.md) properties.</span></span>

