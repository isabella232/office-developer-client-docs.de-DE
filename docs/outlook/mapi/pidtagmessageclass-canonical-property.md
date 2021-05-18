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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359263"
---
# <a name="pidtagmessageclass-canonical-property"></a><span data-ttu-id="7716f-103">PidTagMessageClass (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="7716f-103">PidTagMessageClass Canonical Property</span></span>

  
  
<span data-ttu-id="7716f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7716f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7716f-105">Enthält eine Textzeichenfolge, die die vom Absender definierte Nachrichtenklasse identifiziert, z. B. IPM.Note.</span><span class="sxs-lookup"><span data-stu-id="7716f-105">Contains a text string that identifies the sender-defined message class, such as IPM.Note.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7716f-106">Zugeordnete Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7716f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7716f-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span><span class="sxs-lookup"><span data-stu-id="7716f-107">PR_MESSAGE_CLASS, PR_MESSAGE_CLASS_A, PR_MESSAGE_CLASS_W</span></span>  <br/> |
|<span data-ttu-id="7716f-108">Kennung:</span><span class="sxs-lookup"><span data-stu-id="7716f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7716f-109">0x001A</span><span class="sxs-lookup"><span data-stu-id="7716f-109">0x001A</span></span>  <br/> |
|<span data-ttu-id="7716f-110">Datentyp:</span><span class="sxs-lookup"><span data-stu-id="7716f-110">Data type:</span></span>  <br/> |<span data-ttu-id="7716f-111">PT_UNICODE, PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="7716f-111">PT_UNICODE, PT_STRING8</span></span>  <br/> |
|<span data-ttu-id="7716f-112">Bereich:</span><span class="sxs-lookup"><span data-stu-id="7716f-112">Area:</span></span>  <br/> |<span data-ttu-id="7716f-113">Standard</span><span class="sxs-lookup"><span data-stu-id="7716f-113">Common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7716f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7716f-114">Remarks</span></span>

<span data-ttu-id="7716f-115">Die Nachrichtenklasse gibt den Typ der Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="7716f-115">The message class specifies the type of the message.</span></span> <span data-ttu-id="7716f-116">Sie bestimmt die für die Nachricht definierten Eigenschaften, die Art der von der Nachricht übermittelten Informationen und die Handhabung der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="7716f-116">It determines the set of properties defined for the message, the kind of information the message conveys, and how to handle the message.</span></span> 
  
<span data-ttu-id="7716f-117">Diese Eigenschaften enthalten Zeichenfolgen, die mit Zeiträumen verketten sind.</span><span class="sxs-lookup"><span data-stu-id="7716f-117">These properties contain strings concatenated with periods.</span></span> <span data-ttu-id="7716f-118">Jede Zeichenfolge stellt eine Ebene der Unterklasse dar.</span><span class="sxs-lookup"><span data-stu-id="7716f-118">Each string represents a level of subclassing.</span></span> <span data-ttu-id="7716f-119">Beispiel: IPM. Hinweis ist eine Unterklasse von IPM und eine Superklasse von IPM. Note.Private.</span><span class="sxs-lookup"><span data-stu-id="7716f-119">For example, IPM.Note is a subclass of IPM and a superclass of IPM.Note.Private.</span></span> 
  
<span data-ttu-id="7716f-120">Diese Eigenschaften müssen aus den ASCII-Zeichen 32 bis 127 bestehen und dürfen nicht mit einem Punkt enden (ASCII 46).</span><span class="sxs-lookup"><span data-stu-id="7716f-120">These properties must consist of the ASCII characters 32 through 127 and must not end with a period (ASCII 46).</span></span> <span data-ttu-id="7716f-121">Sortier- und Vergleichsvorgänge müssen als Zeichenfolge ohne Groß-/Kleinschreibung behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="7716f-121">Sort and compare operations must treat it as a case-insensitive string.</span></span> <span data-ttu-id="7716f-122">Die maximal mögliche Länge beträgt 255 Zeichen. Damit MAPI-Raum Qualifizierer angefügt werden kann, wird jedoch empfohlen, die ursprüngliche Länge unter 128 Zeichen zu halten.</span><span class="sxs-lookup"><span data-stu-id="7716f-122">The maximum possible length is 255 characters, but in order to allow MAPI room to append qualifiers it is recommended that the original length be kept under 128 characters.</span></span> 
  
<span data-ttu-id="7716f-123">Jede Nachricht ist erforderlich, um diese Eigenschaften zu senden.</span><span class="sxs-lookup"><span data-stu-id="7716f-123">Every message is required to furnish these properties.</span></span> <span data-ttu-id="7716f-124">Normalerweise legt die Clientanwendung, die eine neue Nachricht erstellt, diese fest, sobald [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) erfolgreich zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7716f-124">Normally, the client application creating a new message sets it as soon as [IMAPIFolder::CreateMessage](imapifolder-createmessage.md) returns successfully.</span></span> <span data-ttu-id="7716f-125">Wenn die Eigenschaft jedoch nicht festgelegt wurde, wenn der Client [IMAPIProp::SaveChanges](imapiprop-savechanges.md)aufruft, sollte der Nachrichtenspeicher sie auf IPM festlegen.</span><span class="sxs-lookup"><span data-stu-id="7716f-125">But if the property has not been set when the client calls [IMAPIProp::SaveChanges](imapiprop-savechanges.md), the message store should set it to IPM.</span></span> 
  
<span data-ttu-id="7716f-126">Die von MAPI definierten Werte sind:</span><span class="sxs-lookup"><span data-stu-id="7716f-126">The values defined by MAPI are:</span></span> 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

<span data-ttu-id="7716f-127">IPM und IPC sind nur als Superklassen vorgesehen, und eine Nachricht sollte mindestens einen Unterklassenqualifizierer angefügt haben, bevor sie gespeichert oder übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="7716f-127">IPM and IPC are intended to be superclasses only, and a message should have at least one subclass qualifier appended before being stored or submitted.</span></span> <span data-ttu-id="7716f-128">Weitere Informationen zur Verwendung von Nachrichtenklassen finden Sie unter [Message Classes](mapi-message-classes.md).</span><span class="sxs-lookup"><span data-stu-id="7716f-128">For more information on message class usage, see [Message Classes](mapi-message-classes.md).</span></span> <span data-ttu-id="7716f-129">Eine Liste der erforderlichen und optionalen Eigenschaften für Nachrichtenklassen finden Sie in den Untertopen von Informationen zu [Nachrichteneigenschaften](message-properties-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7716f-129">For lists of required and optional properties for message classes, see the subtopics of [About Message Properties](message-properties-overview.md).</span></span>
  
<span data-ttu-id="7716f-130">Eine benutzerdefinierte Nachrichtenklasse kann Eigenschaften in einem reservierten Bereich nur für die Verwendung mit dieser Nachrichtenklasse definieren.</span><span class="sxs-lookup"><span data-stu-id="7716f-130">A custom message class can define properties in a reserved range for use with that message class only.</span></span> <span data-ttu-id="7716f-131">Weitere Informationen finden Sie unter [About Property Identifiers](mapi-property-identifier-overview.md).</span><span class="sxs-lookup"><span data-stu-id="7716f-131">For more information, see [About Property Identifiers](mapi-property-identifier-overview.md).</span></span> 
  
<span data-ttu-id="7716f-132">Nachrichtenklassen steuern, in welchem Empfangsordner eine eingehende Nachricht gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="7716f-132">Message classes control which receive folder an incoming message is stored in.</span></span> <span data-ttu-id="7716f-133">Weitere Informationen finden Sie unter [der IMsgStore::GetReceiveFolderTable-Methode.](imsgstore-getreceivefoldertable.md)</span><span class="sxs-lookup"><span data-stu-id="7716f-133">For more information, see the [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) method.</span></span> 
  
<span data-ttu-id="7716f-134">Weitere Informationen zur Verwendung von Nachrichtenklassen mit Formularen und Formularservern finden Sie unter [Choosing a Message Class](choosing-a-message-class.md).</span><span class="sxs-lookup"><span data-stu-id="7716f-134">For more information on using message classes with forms and form servers, see [Choosing a Message Class](choosing-a-message-class.md).</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="7716f-135">Verwandte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7716f-135">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7716f-136">Protokollspezifikationen</span><span class="sxs-lookup"><span data-stu-id="7716f-136">Protocol specifications</span></span>

<span data-ttu-id="7716f-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7716f-137">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7716f-138">Enthält Verweise auf Exchange Server Protokollspezifikationen.</span><span class="sxs-lookup"><span data-stu-id="7716f-138">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7716f-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7716f-139">[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7716f-140">Behandelt Nachrichten- und Anlagenobjekte.</span><span class="sxs-lookup"><span data-stu-id="7716f-140">Handles message and attachment objects.</span></span>
    
<span data-ttu-id="7716f-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7716f-141">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7716f-142">Gibt die Eigenschaften und Vorgänge an, die für E-Mail-Nachrichtenobjekte zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="7716f-142">Specifies the properties and operations that are permissible for email message objects.</span></span>
    
<span data-ttu-id="7716f-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7716f-143">[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7716f-144">Gibt die Eigenschaften und Vorgänge an, die für die Darstellung von Voicemail- und Faxnachrichten zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="7716f-144">Specifies the properties and operations that are permissible for representing voice mail and fax messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7716f-145">Headerdateien</span><span class="sxs-lookup"><span data-stu-id="7716f-145">Header files</span></span>

<span data-ttu-id="7716f-146">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7716f-146">Mapidefs.h</span></span>
  
> <span data-ttu-id="7716f-147">Bietet Datentypdefinitionen.</span><span class="sxs-lookup"><span data-stu-id="7716f-147">Provides data type definitions.</span></span>
    
<span data-ttu-id="7716f-148">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7716f-148">Mapitags.h</span></span>
  
> <span data-ttu-id="7716f-149">Enthält Definitionen von Eigenschaften, die als zugeordnete Eigenschaften aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="7716f-149">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7716f-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7716f-150">See also</span></span>



[<span data-ttu-id="7716f-151">MAPI-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7716f-151">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7716f-152">KANONISCHE EIGENSCHAFTEN VON MAPI</span><span class="sxs-lookup"><span data-stu-id="7716f-152">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7716f-153">Zuordnen kanonischer Eigenschaftsnamen zu MAPI-Namen</span><span class="sxs-lookup"><span data-stu-id="7716f-153">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7716f-154">Zuordnen von MAPI-Namen zu kanonischen Eigenschaftennamen</span><span class="sxs-lookup"><span data-stu-id="7716f-154">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

