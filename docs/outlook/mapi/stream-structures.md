---
title: Streamstrukturen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9e305071-b6a5-4bd8-892e-25553d04bb15
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6ec44fe0dbf8e63b7bbc58da1ba6e20f8ff59d3a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795644"
---
# <a name="stream-structures"></a><span data-ttu-id="39f25-103">Streamstrukturen</span><span class="sxs-lookup"><span data-stu-id="39f25-103">Stream Structures</span></span>

  
  
<span data-ttu-id="39f25-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="39f25-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="39f25-105">Definitionen von benutzerdefinierten Feldern eines Microsoft Outlook-Elements werden in der [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) -Eigenschaft gespeichert.</span><span class="sxs-lookup"><span data-stu-id="39f25-105">Definitions of user-defined fields of a Microsoft Outlook item are stored in the [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) property.</span></span> <span data-ttu-id="39f25-106">Der Wert dieser Eigenschaft ist einen binären Datenstrom, der Definitionen von benutzerdefinierten Feldern und Datenbindung Einstellungen für integrierte Felder sind für das Outlook-Element enthält.</span><span class="sxs-lookup"><span data-stu-id="39f25-106">The value of this property is a binary stream that contains definitions of user-defined fields and data-binding settings for built-in fields for the Outlook item.</span></span> <span data-ttu-id="39f25-107">Dieser Abschnitt enthält Informationen zur Struktur der binären Stream-Objekts, in den folgenden Stream Strukturen aufgeschlüsselt an.</span><span class="sxs-lookup"><span data-stu-id="39f25-107">This section provides information about the structure of the binary stream, broken down in the following stream structures.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="39f25-108">Die Namen der diese Stream-Strukturen (beispielsweise PropertyDefinition FieldDefinition und SkipBlock) und ihre Datenelemente sind nicht technisch gesehen Teil der von der Messaging-API (MAPI)-Programmierschnittstelle und hier nur zu Dokumentationszwecken bereitgestellt werden die tatsächlichen Stream Strukturen Zwecke.</span><span class="sxs-lookup"><span data-stu-id="39f25-108">The names of these stream structures (for example, PropertyDefinition, FieldDefinition, and SkipBlock) and their data elements are not technically part of the programming interface of the Messaging API (MAPI), and are provided here only for documentation purposes of the actual stream structures.</span></span> <span data-ttu-id="39f25-109">Entwickler können diese Stream Strukturen und Daten der Elemente in ihren Anträgen bezeichnen, wie sie auswählen.</span><span class="sxs-lookup"><span data-stu-id="39f25-109">Developers can label these stream structures and data elements in their applications as they choose.</span></span> 
  
- [<span data-ttu-id="39f25-110">PropertyDefinition-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="39f25-110">PropertyDefinition Stream Structure</span></span>](propertydefinition-stream-structure.md)
    
- [<span data-ttu-id="39f25-111">FieldDefinition-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="39f25-111">FieldDefinition Stream Structure</span></span>](fielddefinition-stream-structure.md)
    
- [<span data-ttu-id="39f25-112">SkipBlock-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="39f25-112">SkipBlock Stream Structure</span></span>](skipblock-stream-structure.md)
    
- [<span data-ttu-id="39f25-113">FirstSkipBlockContent-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="39f25-113">FirstSkipBlockContent Stream Structure</span></span>](firstskipblockcontent-stream-structure.md)
    
- [<span data-ttu-id="39f25-114">PackedAnsiString-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="39f25-114">PackedAnsiString Stream Structure</span></span>](packedansistring-stream-structure.md)
    
- [<span data-ttu-id="39f25-115">PackedUnicodeString-Streamstruktur</span><span class="sxs-lookup"><span data-stu-id="39f25-115">PackedUnicodeString Stream Structure</span></span>](packedunicodestring-stream-structure.md)
    
## <a name="see-also"></a><span data-ttu-id="39f25-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39f25-116">See also</span></span>



[<span data-ttu-id="39f25-117">Elemente und Felder in Outlook</span><span class="sxs-lookup"><span data-stu-id="39f25-117">Outlook Items and Fields</span></span>](outlook-items-and-fields.md)
  
[<span data-ttu-id="39f25-118">Hinzufügen einer Definition für ein neues benutzerdefiniertes Feld</span><span class="sxs-lookup"><span data-stu-id="39f25-118">Add a Definition for a New User-Defined Field</span></span>](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[<span data-ttu-id="39f25-119">Beispiel für PropertyDefinition-Stream</span><span class="sxs-lookup"><span data-stu-id="39f25-119">PropertyDefinition Stream Sample</span></span>](propertydefinition-stream-sample.md)

