---
title: PidTagMessageClass (kanonische Eigenschaft)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageClass
api_type:
- HeaderDef
ms.assetid: 1e704023-1992-4b43-857e-0a7da7bc8e87
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7912a3831333ff8a464a12e567430eb5a3272172
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396666"
---
# <a name="pidtagmessageclass-canonical-property"></a><span data-ttu-id="0ab03-103">PidTagMessageClass (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0ab03-103">PidTagMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="0ab03-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0ab03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0ab03-105">Enthält eine Textzeichenfolge, die die Absender benutzerdefinierte Nachrichtenklasse wie IPM identifiziert. Beachten Sie.</span><span class="sxs-lookup"><span data-stu-id="0ab03-105">Contains a text string that identifies the sender-defined message class, such as IPM.Note.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ab03-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="0ab03-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0ab03-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="0ab03-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="0ab03-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="0ab03-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0ab03-109">0x001A</span><span class="sxs-lookup"><span data-stu-id="0ab03-109">0x001A</span></span>  <br/> |
|<span data-ttu-id="0ab03-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="0ab03-110">Data type:</span></span>  <br/> |<span data-ttu-id="0ab03-111">PT_UNICODE PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="0ab03-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="0ab03-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="0ab03-112">Area:</span></span>  <br/> |<span data-ttu-id="0ab03-113">Common</span><span class="sxs-lookup"><span data-stu-id="0ab03-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0ab03-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0ab03-114">Remarks</span></span>

<span data-ttu-id="0ab03-115">Die Nachrichtenklasse gibt den Typ der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0ab03-115">The message class specifies the type of the message.</span></span> <span data-ttu-id="0ab03-116">Bestimmt den Satz von Eigenschaften, die für die Nachricht definiert die Art von Informationen die Nachricht übermittelt, und wie die Meldung zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="0ab03-116">It determines the set of properties defined for the message, the kind of information the message conveys, and how to handle the message.</span></span> 
  
<span data-ttu-id="0ab03-117">Diese Eigenschaften enthalten mit Perioden verkettete Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="0ab03-117">These properties contain strings concatenated with periods.</span></span> <span data-ttu-id="0ab03-118">Jede Zeichenfolge stellt eine Ebene von Unterklassen dar.</span><span class="sxs-lookup"><span data-stu-id="0ab03-118">Each string represents a level of subclassing.</span></span> <span data-ttu-id="0ab03-119">Beispielsweise IPM. Hinweis: ist eine Unterklasse der IPM und eine übergeordnete Klasse von IPM. Note.Private.</span><span class="sxs-lookup"><span data-stu-id="0ab03-119">For example, IPM.Note is a subclass of IPM and a superclass of IPM.Note.Private.</span></span> 
  
<span data-ttu-id="0ab03-120">Diese Eigenschaften müssen den ASCII-Zeichen 32 bis 127 bestehen und darf nicht mit einem Punkt (ASCII-46) enden.</span><span class="sxs-lookup"><span data-stu-id="0ab03-120">These properties must consist of the ASCII characters 32 through 127 and must not end with a period (ASCII 46).</span></span> <span data-ttu-id="0ab03-121">Sortieren und vergleichen Vorgänge müssen sie als ein Zeichenfolgenvergleich behandeln.</span><span class="sxs-lookup"><span data-stu-id="0ab03-121">Sort and compare operations must treat it as a case-insensitive string.</span></span> <span data-ttu-id="0ab03-122">Die maximale mögliche Länge beträgt 255 Zeichen, aber, um MAPI Platz Qualifizierer anzufügende bereitsteht wird empfohlen, dass die ursprüngliche Länge unter 128 Zeichen behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="0ab03-122">The maximum possible length is 255 characters, but in order to allow MAPI room to append qualifiers it is recommended that the original length be kept under 128 characters.</span></span> 
  
<span data-ttu-id="0ab03-123">Jede Nachricht ist erforderlich, um diese Eigenschaften bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="0ab03-123">Every message is required to furnish these properties.</span></span> <span data-ttu-id="0ab03-124">Normalerweise wird die Client-Anwendung eine neue Nachricht erstellen, sobald [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) erfolgreich zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0ab03-124">Normally, the client application creating a new message sets it as soon as [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) returns successfully.</span></span> <span data-ttu-id="0ab03-125">Aber wenn die Eigenschaft, wenn der Client [IMAPIProp::SaveChanges](imapiprop-savechanges.md)ruft nicht festgelegt wurde, der Nachrichtenspeicher sollte auf festlegen IPM.</span><span class="sxs-lookup"><span data-stu-id="0ab03-125">But if the property has not been set when the client calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md), the message store should set it to IPM.</span></span> 
  
<span data-ttu-id="0ab03-126">Die Werte von MAPI definiert sind:</span><span class="sxs-lookup"><span data-stu-id="0ab03-126">The values defined by MAPI are:</span></span> 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

<span data-ttu-id="0ab03-127">IPM und IPK dienen nur Klassen werden, und eine Nachricht sollte mindestens eine Unterklasse Qualifizierer angefügt, bevor Sie gespeichert oder gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="0ab03-127">IPM and IPC are intended to be superclasses only, and a message should have at least one subclass qualifier appended before being stored or submitted.</span></span> <span data-ttu-id="0ab03-128">Weitere Informationen über die Verwendung der Nachricht-Klasse finden Sie unter [Message Classes](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="0ab03-128">For more information on message class usage, see [Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="0ab03-129">Liste der erforderlichen und optionalen Eigenschaften für Nachrichtenklassen finden Sie unter der untergeordneten Themen mit [Informationen zu Nachrichteneigenschaften](message-properties-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0ab03-129">For lists of required and optional properties for message classes, see the subtopics of [About Message Properties](message-properties-overview.md).</span></span>
  
<span data-ttu-id="0ab03-130">Eine benutzerdefinierte Nachrichtenklasse kann Eigenschaften in einem reservierten Bereich für die Verwendung mit nur die Nachrichtenklasse definieren.</span><span class="sxs-lookup"><span data-stu-id="0ab03-130">A custom message class can define properties in a reserved range for use with that message class only.</span></span> <span data-ttu-id="0ab03-131">Weitere Informationen finden Sie unter [Informationen zu Eigenschaftskennungen](mapi-property-identifier-overview.md).</span><span class="sxs-lookup"><span data-stu-id="0ab03-131">For more information, see [About Property Identifiers](mapi-property-identifier-overview.md).</span></span> 
  
<span data-ttu-id="0ab03-132">Nachricht Klassen steuern, welche die Ordner eine eingehende Nachricht empfangen wird in gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0ab03-132">Message classes control which receive folder an incoming message is stored in.</span></span> <span data-ttu-id="0ab03-133">Weitere Informationen finden Sie unter der [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0ab03-133">For more information, see the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="0ab03-134">Weitere Informationen zur Verwendung von Nachrichtenklassen mit Formularen und Form-Servern finden Sie unter [Auswählen einer Nachrichtenklasse](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="0ab03-134">For more information on using message classes with forms and form servers, see [Choosing a Message Class](choosing-a-message-class.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0ab03-135">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0ab03-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0ab03-136">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="0ab03-136">Protocol specifications</span></span>

<span data-ttu-id="0ab03-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ab03-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ab03-138">Bietet Verweise auf Verwandte Exchange Server-Spezifikationen.</span><span class="sxs-lookup"><span data-stu-id="0ab03-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0ab03-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ab03-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ab03-140">Nachrichten und Anlagen Objekte behandelt.</span><span class="sxs-lookup"><span data-stu-id="0ab03-140">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="0ab03-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ab03-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ab03-142">Gibt die Eigenschaften und Operationen, die für e-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0ab03-142">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="0ab03-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0ab03-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0ab03-144">Gibt die Eigenschaften und Operationen, die für das Darstellen von Voicemail- und Sprachnachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="0ab03-144">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0ab03-145">Header-Dateien</span><span class="sxs-lookup"><span data-stu-id="0ab03-145">Header files</span></span>

<span data-ttu-id="0ab03-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0ab03-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="0ab03-147">Enthält die Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="0ab03-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="0ab03-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0ab03-148">Mapitags.h</span></span>
  
> <span data-ttu-id="0ab03-149">Enthält Definitionen von Eigenschaften, die als zugeordneten Eigenschaften aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="0ab03-149">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0ab03-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0ab03-150">See also</span></span>



[<span data-ttu-id="0ab03-151">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0ab03-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0ab03-152">Kanonische MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="0ab03-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0ab03-153">Zuordnen von kanonischen Eigenschaftennamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="0ab03-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0ab03-154">Zuordnen von MAPI-Namen zu kanonische Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="0ab03-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

