---
title: Streamstrukturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5f372e93457f2b7ef8830ae6bd0363f6b3a7bd60
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581580"
---
# <a name="stream-structures"></a><span data-ttu-id="8aa81-103">Streamstrukturen</span><span class="sxs-lookup"><span data-stu-id="8aa81-103">Stream Structures</span></span>

  
  
<span data-ttu-id="8aa81-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8aa81-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8aa81-105">Definitionen von benutzerdefinierten Feldern eines Microsoft Outlook-Elements werden in der [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) -Eigenschaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8aa81-105">Definitions of user-defined fields of a Microsoft Outlook item are stored in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property.</span></span> <span data-ttu-id="8aa81-106">Der Wert dieser Eigenschaft ist einen binären Datenstrom, der Definitionen von benutzerdefinierten Feldern und Datenbindung Einstellungen für integrierte Felder sind für das Outlook-Element enthält.</span><span class="sxs-lookup"><span data-stu-id="8aa81-106">The value of this property is a binary stream that contains definitions of user-defined fields and data-binding settings for built-in fields for the Outlook item.</span></span> <span data-ttu-id="8aa81-107">Dieser Abschnitt enthält Informationen zur Struktur der binären Stream-Objekts, in den folgenden Stream Strukturen aufgeschlüsselt an.</span><span class="sxs-lookup"><span data-stu-id="8aa81-107">This section provides information about the structure of the binary stream, broken down in the following stream structures.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="8aa81-108">Die Namen der diese Stream-Strukturen (beispielsweise PropertyDefinition FieldDefinition und SkipBlock) und ihre Datenelemente sind nicht technisch gesehen Teil der von der Messaging-API (MAPI)-Programmierschnittstelle und hier nur zu Dokumentationszwecken bereitgestellt werden die tatsächlichen Stream Strukturen Zwecke.</span><span class="sxs-lookup"><span data-stu-id="8aa81-108">The names of these stream structures (for example, PropertyDefinition, FieldDefinition, and SkipBlock) and their data elements are not technically part of the programming interface of the Messaging API (MAPI), and are provided here only for documentation purposes of the actual stream structures.</span></span> <span data-ttu-id="8aa81-109">Entwickler können diese Stream Strukturen und Daten der Elemente in ihren Anträgen bezeichnen, wie sie auswählen.</span><span class="sxs-lookup"><span data-stu-id="8aa81-109">Developers can label these stream structures and data elements in their applications as they choose.</span></span> 
  
- [<span data-ttu-id="8aa81-110">PropertyDefinition-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="8aa81-110">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
    
- [<span data-ttu-id="8aa81-111">FieldDefinition-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="8aa81-111">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
    
- [<span data-ttu-id="8aa81-112">SkipBlock-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="8aa81-112">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
    
- [<span data-ttu-id="8aa81-113">FirstSkipBlockContent-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="8aa81-113">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
    
- [<span data-ttu-id="8aa81-114">PackedAnsiString-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="8aa81-114">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
    
- [<span data-ttu-id="8aa81-115">PackedUnicodeString-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="8aa81-115">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a><span data-ttu-id="8aa81-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8aa81-116">See also</span></span>



[<span data-ttu-id="8aa81-117">Elemente und Felder in Outlook</span><span class="sxs-lookup"><span data-stu-id="8aa81-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="8aa81-118">Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld</span><span class="sxs-lookup"><span data-stu-id="8aa81-118">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="8aa81-119">Beispiel für PropertyDefinition-Stream</span><span class="sxs-lookup"><span data-stu-id="8aa81-119">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)

