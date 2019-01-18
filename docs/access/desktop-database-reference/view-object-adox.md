---
title: View-Objekt (ADOX - Access-desktop-Datenbank (engl.))
TOCTitle: View object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3b5d25a727233b5fda5627df8dff952003bbfe3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28722473"
---
# <a name="view-object-adox"></a><span data-ttu-id="ec39f-102">View-Objekt (ADOX)</span><span class="sxs-lookup"><span data-stu-id="ec39f-102">View object (ADOX)</span></span>


<span data-ttu-id="ec39f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ec39f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ec39f-p101">Stellt eine gefilterte Datensatzgruppe oder eine virtuelle Tabelle dar. Wenn es in Verbindung mit dem ADO-Objekt [Command](command-object-ado.md) verwendet wird, kann das **View** -Objekt zum Hinzufügen, Löschen oder Ändern von Sichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ec39f-p101">Represents a filtered set of records or a virtual table. When used in conjunction with the ADO [Command](command-object-ado.md) object, the **View** object can be used for adding, deleting, or modifying views.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec39f-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ec39f-106">Remarks</span></span>

<span data-ttu-id="ec39f-p102">Eine Sicht ist eine virtuelle Tabelle, die aus anderen Datenbanktabellen oder -sichten erstellt wird. Mit dem **View** -Objekt können Sie eine Sicht erstellen, ohne die CREATE VIEW-Syntax des Anbieters zu kennen oder zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec39f-p102">A view is a virtual table, created from other database tables or views. The **View** object allows you to create a view without having to know or use the provider's "CREATE VIEW" syntax.</span></span>

<span data-ttu-id="ec39f-109">Die Eigenschaften eines **View** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ec39f-109">With the properties of a **View** object, you can:</span></span>

  - <span data-ttu-id="ec39f-110">Identifizieren der Sicht, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec39f-110">Identify the view with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="ec39f-111">Angeben des ADO-Objekts **Command**, das zum Hinzufügen, Löschen oder Ändern von Sichten verwendet werden kann, indem Sie die [Command](command-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec39f-111">Specify the ADO **Command** object that can be used to add, delete, or modify views with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="ec39f-112">Zurückgeben von Datumsinformationen, indem Sie die Eigenschaften [DateCreated](datecreated-property-adox.md) und [DateModified](datemodified-property-adox.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="ec39f-112">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

