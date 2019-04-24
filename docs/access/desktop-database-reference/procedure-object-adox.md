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
# <a name="procedure-object-adox"></a><span data-ttu-id="68e28-102">Procedure-Objekt (ADOX)</span><span class="sxs-lookup"><span data-stu-id="68e28-102">Procedure object (ADOX)</span></span>


<span data-ttu-id="68e28-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="68e28-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="68e28-p101">Stellt eine gespeicherte Prozedur dar. Wenn es in Verbindung mit dem ADO-Objekt [Command](command-object-ado.md) verwendet wird, kann das **Procedure** -Objekt zum Hinzufügen, Löschen oder Ändern von gespeicherten Prozeduren verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="68e28-p101">Represents a stored procedure. When used in conjunction with the ADO [Command](command-object-ado.md) object, the **Procedure** object can be used for adding, deleting, or modifying stored procedures.</span></span>

## <a name="remarks"></a><span data-ttu-id="68e28-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="68e28-106">Remarks</span></span>

<span data-ttu-id="68e28-107">Mit dem **Procedure**-Objekt können Sie eine gespeicherte Prozedur erstellen, ohne die CREATE PROCEDURE-Syntax des Anbieters zu kennen oder zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="68e28-107">The **Procedure** object allows you to create a stored procedure without having to know or use the provider's "CREATE PROCEDURE" syntax.</span></span>

<span data-ttu-id="68e28-108">Die Eigenschaften eines **Procedure** -Objekts ermöglichen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="68e28-108">With the properties of a **Procedure** object, you can:</span></span>

  - <span data-ttu-id="68e28-109">Identifizieren der Prozedur, indem Sie die [Name](name-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="68e28-109">Identify the procedure with the [Name](name-property-adox.md) property.</span></span>

  - <span data-ttu-id="68e28-110">Angeben des ADO-Objekts **Command**, das zum Erstellen oder Ausführen der Prozedur verwendet werden kann, indem Sie die [Command](command-property-adox.md)-Eigenschaft verwenden.</span><span class="sxs-lookup"><span data-stu-id="68e28-110">Specify the ADO **Command** object that can be used to create or execute the procedure with the [Command](command-property-adox.md) property.</span></span>

  - <span data-ttu-id="68e28-111">Zurückgeben von Datumsinformationen, indem Sie die Eigenschaften [DateCreated](datecreated-property-adox.md) und [DateModified](datemodified-property-adox.md) verwenden.</span><span class="sxs-lookup"><span data-stu-id="68e28-111">Return date information with the [DateCreated](datecreated-property-adox.md) and [DateModified](datemodified-property-adox.md) properties.</span></span>

