---
title: Key-Objekt (ADOX - Access-desktop-Datenbank (engl.))
TOCTitle: Key Object (ADOX)
ms:assetid: 727198ec-57d2-7766-790c-370beb931de6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249461(v=office.15)
ms:contentKeyID: 48545608
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2edda6dfe7dd9ec28f3eb4cb11714d59806c80e0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25871360"
---
# <a name="key-object-adox"></a><span data-ttu-id="f2fb7-102">Key-Objekt (ADOX)</span><span class="sxs-lookup"><span data-stu-id="f2fb7-102">Key Object (ADOX)</span></span>


<span data-ttu-id="f2fb7-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f2fb7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f2fb7-104">Stellt ein Primärschlüsselfeld, ein Fremdschlüsselfeld oder ein Feld für einen eindeutigen Schlüssel aus einer Datenbanktabelle dar.</span><span class="sxs-lookup"><span data-stu-id="f2fb7-104">Represents a primary, foreign, or unique key field from a database table.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2fb7-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f2fb7-105">Remarks</span></span>

<span data-ttu-id="f2fb7-106">Mit dem folgenden Code wird ein neues **Key** -Objekt erstellt:</span><span class="sxs-lookup"><span data-stu-id="f2fb7-106">The following code creates a new **Key**:</span></span>

`Dim obj As New Key`

<span data-ttu-id="f2fb7-107">Die Eigenschaften und Auflistungen eines **Key** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f2fb7-107">With the properties and collections of a **Key** object, you can:</span></span>

- <span data-ttu-id="f2fb7-108">Identifizieren des Schlüssels, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2fb7-108">Identify the key with the [Name](name-property-adox.md) property.</span></span>

- <span data-ttu-id="f2fb7-109">Bestimmen, ob es sich um einen Primär- oder Fremdschlüssel oder um einen eindeutigen Schlüssel handelt, indem Sie die [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\))-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2fb7-109">Determine whether the key is primary, foreign, or unique with the [Type](https://msdn.microsoft.com/library/jj248879\(v=office.15\)) property.</span></span>

- <span data-ttu-id="f2fb7-110">Zugreifen auf die Datenbankspalten des Schlüssels, indem Sie die [Columns](columns-collection-adox.md)-Auflistung verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2fb7-110">Access the database columns of the key with the [Columns](columns-collection-adox.md) collection.</span></span>

- <span data-ttu-id="f2fb7-111">Angeben des Namens der verwandten Tabelle, indem Sie die [RelatedTable](relatedtable-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2fb7-111">Specify the name of the related table with the [RelatedTable](relatedtable-property-adox.md) property.</span></span>

- <span data-ttu-id="f2fb7-112">Bestimmen der Aktion, die beim Löschen oder Aktualisieren des Primärschlüssels ausgeführt wird, indem Sie die Eigenschaften [DeleteRule](deleterule-property-adox.md) und [UpdateRule](updaterule-property-adox.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2fb7-112">Determine the action performed on deletion or update of a primary key with the [DeleteRule](deleterule-property-adox.md) and [UpdateRule](updaterule-property-adox.md) properties.</span></span>

