---
title: Fügen Sie eine Definition für ein neues benutzerdefiniertes Feld hinzu
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 183d3b86-4506-44da-bbfc-d6242ad89e57
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 26c329323eebff6cfdf4f4be4dffe9a62f8745e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791834"
---
# <a name="add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="d498b-103">Fügen Sie eine Definition für ein neues benutzerdefiniertes Feld hinzu</span><span class="sxs-lookup"><span data-stu-id="d498b-103">Add a definition for a new user-defined field</span></span>
 
<span data-ttu-id="d498b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d498b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d498b-105">Wenn Sie ein benutzerdefiniertes Feld mit einem Microsoft Outlook-Element hinzufügen, fügen Sie eine Definition für ein Feld in der entsprechenden [PropertyDefinition](propertydefinition-stream-structure.md) Stream-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d498b-105">When you add a user-defined field to a Microsoft Outlook item, you add a field definition to the corresponding [PropertyDefinition](propertydefinition-stream-structure.md) stream structure.</span></span> <span data-ttu-id="d498b-106">Verwenden Sie das folgende Verfahren so eine PropertyDefinition Stream-Struktur einer neuen Definition für ein Feld hinzu.</span><span class="sxs-lookup"><span data-stu-id="d498b-106">Use the following procedure to add a new field definition to a PropertyDefinition stream structure.</span></span> 
  
### <a name="to-add-a-definition-for-a-new-user-defined-field"></a><span data-ttu-id="d498b-107">So fügen Sie eine Definition für ein neues benutzerdefiniertes Feld hinzu</span><span class="sxs-lookup"><span data-stu-id="d498b-107">To add a definition for a new user-defined field</span></span>

1. <span data-ttu-id="d498b-108">Kopieren Sie die vorhandenen Felddefinitionen der Struktur PropertyDefinition Stream in ein neues Feld Definitionen Array.</span><span class="sxs-lookup"><span data-stu-id="d498b-108">Copy the existing field definitions of the PropertyDefinition stream structure to a new field definitions array.</span></span> 
    
2. <span data-ttu-id="d498b-109">Wenn alle vorhandenen Felddefinitionen im Format PropDefV1 sind, konvertieren Sie sie in das PropDefV2-Format.</span><span class="sxs-lookup"><span data-stu-id="d498b-109">If any existing field definitions are in the PropDefV1 format, convert them to the PropDefV2 format.</span></span> <span data-ttu-id="d498b-110">Weitere Informationen zu Feldformate Definition finden Sie unter [PropertyDefinition Stream](propertydefinition-stream-structure.md) auch [FieldDefinition Stream Struktur](fielddefinition-stream-structure.md).</span><span class="sxs-lookup"><span data-stu-id="d498b-110">For more information about field definition formats, see [PropertyDefinition Stream Structure](propertydefinition-stream-structure.md) and [FieldDefinition Stream Structure](fielddefinition-stream-structure.md).</span></span>
    
3. <span data-ttu-id="d498b-111">Erstellen Sie eine Definition des neuen benutzerdefinierten Felds im Format PropDefV2 und fügen Sie es in das Array.</span><span class="sxs-lookup"><span data-stu-id="d498b-111">Create a definition of the new user-defined field in the PropDefV2 format and add it to the array.</span></span>
    
4. <span data-ttu-id="d498b-112">Legen Sie das Version-Element der Struktur Stream PropertyDefinition als 0x0103, wenn das Version-Element mit diesem Wert nicht festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="d498b-112">Set the Version element of the PropertyDefinition stream structure as 0x0103, if the Version element has not been set to that value.</span></span>
    
5. <span data-ttu-id="d498b-113">Das Element FieldDefinitionCount um 1 erhöht.</span><span class="sxs-lookup"><span data-stu-id="d498b-113">Increment the FieldDefinitionCount element by 1.</span></span>
    
6. <span data-ttu-id="d498b-114">Speichern Sie das Array als Wert des FieldDefinitions-Elements.</span><span class="sxs-lookup"><span data-stu-id="d498b-114">Store the array as the value of the FieldDefinitions element.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d498b-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d498b-115">See also</span></span>

- [<span data-ttu-id="d498b-116">PropertyDefinition-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="d498b-116">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)

