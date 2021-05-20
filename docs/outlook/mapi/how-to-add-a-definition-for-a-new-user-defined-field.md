---
title: Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2879299d152d8fea7690162ae55a22f337f5fd59
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428165"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="919ea-103">Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld</span><span class="sxs-lookup"><span data-stu-id="919ea-103">Add a definition for a new user-defined field</span></span>
 
<span data-ttu-id="919ea-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="919ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="919ea-105">Wenn Sie ein benutzerdefiniertes Feld zu einem Microsoft Outlook hinzufügen, fügen Sie der entsprechenden [PropertyDefinition-Streamstruktur](propertydefinition-stream-structure.md) eine Felddefinition hinzu.</span><span class="sxs-lookup"><span data-stu-id="919ea-105">When you add a user-defined field to a Microsoft Outlook item, you add a field definition to the corresponding [PropertyDefinition](propertydefinition-stream-structure.md) stream structure.</span></span> <span data-ttu-id="919ea-106">Verwenden Sie das folgende Verfahren, um einer PropertyDefinition-Streamstruktur eine neue Felddefinition hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="919ea-106">Use the following procedure to add a new field definition to a PropertyDefinition stream structure.</span></span> 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="919ea-107">So fügen Sie eine Definition für ein neues benutzerdefiniertes Feld hinzu</span><span class="sxs-lookup"><span data-stu-id="919ea-107">To add a definition for a new user-defined field</span></span>

1. <span data-ttu-id="919ea-108">Kopieren Sie die vorhandenen Felddefinitionen der PropertyDefinition-Streamstruktur in ein neues Felddefinitionsarray.</span><span class="sxs-lookup"><span data-stu-id="919ea-108">Copy the existing field definitions of the PropertyDefinition stream structure to a new field definitions array.</span></span> 
    
2. <span data-ttu-id="919ea-109">Wenn sich vorhandene Felddefinitionen im PropDefV1-Format befinden, konvertieren Sie sie in das PropDefV2-Format.</span><span class="sxs-lookup"><span data-stu-id="919ea-109">If any existing field definitions are in the PropDefV1 format, convert them to the PropDefV2 format.</span></span> <span data-ttu-id="919ea-110">Weitere Informationen zu Felddefinitionsformaten finden Sie unter [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) und [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="919ea-110">For more information about field definition formats, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) and [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
    
3. <span data-ttu-id="919ea-111">Erstellen Sie eine Definition des neuen benutzerdefinierten Felds im PropDefV2-Format, und fügen Sie es dem Array hinzu.</span><span class="sxs-lookup"><span data-stu-id="919ea-111">Create a definition of the new user-defined field in the PropDefV2 format and add it to the array.</span></span>
    
4. <span data-ttu-id="919ea-112">Legen Sie das Version-Element der PropertyDefinition-Streamstruktur als 0x0103 fest, wenn das Version-Element nicht auf den Wert festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="919ea-112">Set the Version element of the PropertyDefinition stream structure as 0x0103, if the Version element has not been set to that value.</span></span>
    
5. <span data-ttu-id="919ea-113">Erhöhen Sie das FieldDefinitionCount-Element um 1.</span><span class="sxs-lookup"><span data-stu-id="919ea-113">Increment the FieldDefinitionCount element by 1.</span></span>
    
6. <span data-ttu-id="919ea-114">Store array als Wert des FieldDefinitions-Elements.</span><span class="sxs-lookup"><span data-stu-id="919ea-114">Store the array as the value of the FieldDefinitions element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="919ea-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="919ea-115">See also</span></span>

- [<span data-ttu-id="919ea-116">PropertyDefinition Stream Structure</span><span class="sxs-lookup"><span data-stu-id="919ea-116">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)

