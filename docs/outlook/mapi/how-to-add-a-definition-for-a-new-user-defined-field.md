---
title: Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2879299d152d8fea7690162ae55a22f337f5fd59
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299069"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="990a9-103">Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld</span><span class="sxs-lookup"><span data-stu-id="990a9-103">Add a definition for a new user-defined field</span></span>
 
<span data-ttu-id="990a9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="990a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="990a9-105">Wenn Sie einem Microsoft Outlook-Element ein benutzerdefiniertes Feld hinzufügen, fügen Sie der entsprechenden [PropertyDefinition](propertydefinition-stream-structure.md) -Datenstrom Struktur eine Felddefinition hinzu.</span><span class="sxs-lookup"><span data-stu-id="990a9-105">When you add a user-defined field to a Microsoft Outlook item, you add a field definition to the corresponding [PropertyDefinition](propertydefinition-stream-structure.md) stream structure.</span></span> <span data-ttu-id="990a9-106">Verwenden Sie das folgende Verfahren, um einer PropertyDefinition-Datenstrom Struktur eine neue Felddefinition hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="990a9-106">Use the following procedure to add a new field definition to a PropertyDefinition stream structure.</span></span> 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="990a9-107">So fügen Sie eine Definition für ein neues benutzerdefiniertes Feld hinzu</span><span class="sxs-lookup"><span data-stu-id="990a9-107">To add a definition for a new user-defined field</span></span>

1. <span data-ttu-id="990a9-108">Kopieren Sie die vorhandenen Felddefinitionen der PropertyDefinition-Datenstrom Struktur in ein neues Feld Definitions Array.</span><span class="sxs-lookup"><span data-stu-id="990a9-108">Copy the existing field definitions of the PropertyDefinition stream structure to a new field definitions array.</span></span> 
    
2. <span data-ttu-id="990a9-109">Wenn vorhandene Felddefinitionen im PropDefV1-Format vorliegen, konvertieren Sie Sie in das PropDefV2-Format.</span><span class="sxs-lookup"><span data-stu-id="990a9-109">If any existing field definitions are in the PropDefV1 format, convert them to the PropDefV2 format.</span></span> <span data-ttu-id="990a9-110">Weitere Informationen zu Feld Definitions Formaten finden Sie unter [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) und [FieldDefinition streamstruktur Stream Structure](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="990a9-110">For more information about field definition formats, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) and [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
    
3. <span data-ttu-id="990a9-111">Erstellen Sie eine Definition des neuen benutzerdefinierten Felds im PropDefV2-Format, und fügen Sie Sie dem Array hinzu.</span><span class="sxs-lookup"><span data-stu-id="990a9-111">Create a definition of the new user-defined field in the PropDefV2 format and add it to the array.</span></span>
    
4. <span data-ttu-id="990a9-112">Legen Sie das Version-Element der PropertyDefinition-Datenstrom Struktur als 0x0103 fest, wenn das Version-Element nicht auf diesen Wert festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="990a9-112">Set the Version element of the PropertyDefinition stream structure as 0x0103, if the Version element has not been set to that value.</span></span>
    
5. <span data-ttu-id="990a9-113">Inkrementieren Sie das FieldDefinitionCount-Element um 1.</span><span class="sxs-lookup"><span data-stu-id="990a9-113">Increment the FieldDefinitionCount element by 1.</span></span>
    
6. <span data-ttu-id="990a9-114">Speichern Sie das Array als Wert des FieldDefinitions-Elements.</span><span class="sxs-lookup"><span data-stu-id="990a9-114">Store the array as the value of the FieldDefinitions element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="990a9-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="990a9-115">See also</span></span>

- [<span data-ttu-id="990a9-116">PropertyDefinition-Datenstrom Struktur</span><span class="sxs-lookup"><span data-stu-id="990a9-116">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)

