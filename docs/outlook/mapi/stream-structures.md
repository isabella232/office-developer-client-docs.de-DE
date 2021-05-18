---
title: Streamstrukturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 7f1f1e028797edaa0afb45df4f39aca15ff6d425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407823"
---
# <a name="stream-structures"></a><span data-ttu-id="e2f9a-103">Streamstrukturen</span><span class="sxs-lookup"><span data-stu-id="e2f9a-103">Stream Structures</span></span>

  
  
<span data-ttu-id="e2f9a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2f9a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2f9a-105">Definitionen von benutzerdefinierten Feldern eines Microsoft Outlook werden in der [PidLidPropertyDefinitionStream-Eigenschaft](pidlidpropertydefinitionstream-canonical-property.md) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e2f9a-105">Definitions of user-defined fields of a Microsoft Outlook item are stored in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property.</span></span> <span data-ttu-id="e2f9a-106">Der Wert dieser Eigenschaft ist ein binärer Datenstrom, der Definitionen von benutzerdefinierten Feldern und Datenbindungseinstellungen für integrierte Felder für das Outlook enthält.</span><span class="sxs-lookup"><span data-stu-id="e2f9a-106">The value of this property is a binary stream that contains definitions of user-defined fields and data-binding settings for built-in fields for the Outlook item.</span></span> <span data-ttu-id="e2f9a-107">Dieser Abschnitt enthält Informationen zur Struktur des binären Datenstroms, die in den folgenden Datenstromstrukturen aufgeschlüsselt sind.</span><span class="sxs-lookup"><span data-stu-id="e2f9a-107">This section provides information about the structure of the binary stream, broken down in the following stream structures.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e2f9a-108">Die Namen dieser Streamstrukturen (z. B. PropertyDefinition, FieldDefinition und SkipBlock) und deren Datenelemente sind technisch nicht Teil der Programmierschnittstelle der Messaging-API (MAPI) und werden hier nur zu Dokumentationszwecken der tatsächlichen Streamstrukturen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="e2f9a-108">The names of these stream structures (for example, PropertyDefinition, FieldDefinition, and SkipBlock) and their data elements are not technically part of the programming interface of the Messaging API (MAPI), and are provided here only for documentation purposes of the actual stream structures.</span></span> <span data-ttu-id="e2f9a-109">Entwickler können diese Datenstromstrukturen und Datenelemente in ihren Anwendungen nach Wahl beschriften.</span><span class="sxs-lookup"><span data-stu-id="e2f9a-109">Developers can label these stream structures and data elements in their applications as they choose.</span></span> 
  
- [<span data-ttu-id="e2f9a-110">PropertyDefinition Stream Structure</span><span class="sxs-lookup"><span data-stu-id="e2f9a-110">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
    
- [<span data-ttu-id="e2f9a-111">FieldDefinition Stream Structure</span><span class="sxs-lookup"><span data-stu-id="e2f9a-111">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
    
- [<span data-ttu-id="e2f9a-112">SkipBlock Stream Structure</span><span class="sxs-lookup"><span data-stu-id="e2f9a-112">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
    
- [<span data-ttu-id="e2f9a-113">FirstSkipBlockContent Stream Structure</span><span class="sxs-lookup"><span data-stu-id="e2f9a-113">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
    
- [<span data-ttu-id="e2f9a-114">PackedAnsiString-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="e2f9a-114">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
    
- [<span data-ttu-id="e2f9a-115">PackedUnicodeString-Datenstromstruktur</span><span class="sxs-lookup"><span data-stu-id="e2f9a-115">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a><span data-ttu-id="e2f9a-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2f9a-116">See also</span></span>



[<span data-ttu-id="e2f9a-117">Outlook Elemente und Felder</span><span class="sxs-lookup"><span data-stu-id="e2f9a-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="e2f9a-118">Hinzufügen einer Definition für ein new User-Defined Field</span><span class="sxs-lookup"><span data-stu-id="e2f9a-118">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="e2f9a-119">PropertyDefinition Stream Sample</span><span class="sxs-lookup"><span data-stu-id="e2f9a-119">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)

