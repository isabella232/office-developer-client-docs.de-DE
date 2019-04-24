---
title: View-Objekt (ADOX-Access-Desktop-Daten Bankreferenz)
TOCTitle: View object (ADOX)
ms:assetid: 3b2e9972-8a0d-eaa3-1c93-ae0665a47f02
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249149(v=office.15)
ms:contentKeyID: 48544280
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b3b5d25a727233b5fda5627df8dff952003bbfe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306049"
---
# <a name="view-object-adox"></a><span data-ttu-id="0a63d-102">View-Objekt (ADOX)</span><span class="sxs-lookup"><span data-stu-id="0a63d-102">View object (ADOX)</span></span>


<span data-ttu-id="0a63d-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0a63d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0a63d-p101">Stellt eine gefilterte Datensatzgruppe oder eine virtuelle Tabelle dar. Wenn es in Verbindung mit dem ADO-Objekt [Command](command-object-ado.md) verwendet wird, kann das **View** -Objekt zum Hinzufügen, Löschen oder Ändern von Sichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0a63d-p101">Represents a filtered set of records or a virtual table. When used in conjunction with the ADO [Command](command-object-ado.md) object, the **View** object can be used for adding, deleting, or modifying views.</span></span>

## <a name="remarks"></a><span data-ttu-id="0a63d-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a63d-106">Remarks</span></span>

<span data-ttu-id="0a63d-p102">Eine Sicht ist eine virtuelle Tabelle, die aus anderen Datenbanktabellen oder -sichten erstellt wird. Mit dem **View** -Objekt können Sie eine Sicht erstellen, ohne die CREATE VIEW-Syntax des Anbieters zu kennen oder zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="0a63d-p102">A view is a virtual table, created from other database tables or views. The **View** object allows you to create a view without having to know or use the provider's "CREATE VIEW" syntax.</span></span>

<span data-ttu-id="0a63d-109">Die Eigenschaften eines **View** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0a63d-109">With the properties of a **View** object, you can:</span></span>

  - <span data-ttu-id="0a63d-110">Identifizieren der Sicht, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="0a63d-110">Identify the view with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="0a63d-111">Angeben des ADO-Objekts **Command**, das zum Hinzufügen, Löschen oder Ändern von Sichten verwendet werden kann, indem Sie die [Command](command-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="0a63d-111">Specify the ADO **Command** object that can be used to add, delete, or modify views with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="0a63d-112">Zurückgeben von Datumsinformationen, indem Sie die Eigenschaften [DateCreated](datecreated-property-adox.md) und [DateModified](datemodified-property-adox.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="0a63d-112">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

