---
title: TNEF-Verarbeitung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d324fb3-d917-4502-b3a4-179c479deb79
description: 'Letzte Änderung: Donnerstag, 5. Juli 2012'
ms.openlocfilehash: bd9cc49f5d1d865d5d6b222677df0dd62ec36fd6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795732"
---
# <a name="tnef-processing"></a><span data-ttu-id="1de68-103">TNEF-Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="1de68-103">TNEF Processing</span></span>

  
  
<span data-ttu-id="1de68-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1de68-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1de68-105">Die folgende Reihe von Aktionen wird beschrieben, wie Transporten TNEF-Methoden zum Verarbeiten von eingehender und ausgehender Nachrichten verwenden.</span><span class="sxs-lookup"><span data-stu-id="1de68-105">The following series of actions describe how transports use TNEF methods to process outgoing and incoming messages.</span></span>
  
 <span data-ttu-id="1de68-106">**Senden eine Nachricht, die einen TNEF-Stream enthält**</span><span class="sxs-lookup"><span data-stu-id="1de68-106">**To send a message that includes a TNEF stream**</span></span>
  
1. <span data-ttu-id="1de68-107">Verarbeiten von den Eigenschaften der Nachricht, die von der messaging-System unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1de68-107">Process the message properties that are supported by the messaging system.</span></span>
    
2. <span data-ttu-id="1de68-108">Markieren Sie die Nachricht in einer Implementierung bestimmte Weise, damit der empfangenden Adressbuchhierarchie ermitteln kann, dass die Nachricht TNEF-Verarbeitung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1de68-108">Mark the message in an implementation specific way so that the receiving transport provider can determine that the message requires TNEF processing.</span></span> <span data-ttu-id="1de68-109">Eine TNEF-Transportdienst senden an eine SMTP-messaging-System möglicherweise beispielsweise ein benutzerdefinierter Header-Feld wie "X-enthält-TNEF" um anzugeben, dass die Nachricht TNEF-Daten enthält hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1de68-109">For example, a TNEF transport provider sending to an SMTP messaging system might add a custom header field like "X-CONTAINS-TNEF" to indicate that the message contains TNEF data.</span></span>
    
3. <span data-ttu-id="1de68-110">Abrufen eines TNEF-Objekts, und verwenden Sie es zum Kapseln der Nachrichteneigenschaften von messaging-System in einem Stream TNEF nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1de68-110">Obtain a TNEF object and use it to encapsulate the message properties not supported by the messaging system into a TNEF stream.</span></span>
    
4. <span data-ttu-id="1de68-111">Codieren Sie mit der messaging-System Anlage Objektmodell TNEF-Stream.</span><span class="sxs-lookup"><span data-stu-id="1de68-111">Encode the TNEF stream using the messaging system's attachment model.</span></span> <span data-ttu-id="1de68-112">Beispielsweise wenn das zugrunde liegende Anlage Modell Uuencode Anlagen und den Nachrichtentext anfügen, muss dann der Adressbuchhierarchie Uuencode TNEF-Stream in einer anderen Anlage.</span><span class="sxs-lookup"><span data-stu-id="1de68-112">For example, if the underlying attachment model is to uuencode attachments and append them to the message text, then the transport provider must uuencode the TNEF stream into another attachment.</span></span> <span data-ttu-id="1de68-113">Der Transportdienst muss auch eine Methode für die Erkennung von welche Anlage den codierten TNEF-Stream enthält, wenn sie eine Nachricht empfängt implementieren.</span><span class="sxs-lookup"><span data-stu-id="1de68-113">The transport provider must also implement a method for recognizing which attachment contains the encoded TNEF stream when it receives a message.</span></span> <span data-ttu-id="1de68-114">Standardverfahren zum Kennzeichnen dieser Anlage ist, damit es erhält ein Dateiname der Anlage von "WINMAIL. FILTERN".</span><span class="sxs-lookup"><span data-stu-id="1de68-114">The standard way to mark this attachment is to give it an attachment filename of "WINMAIL.DAT".</span></span> <span data-ttu-id="1de68-115">Wenn der Adressbuchhierarchie dies der Fall ist, werden können mit ihm interagieren alle Transportanbieter TNEF-aktiviert, die dieser Konvention.</span><span class="sxs-lookup"><span data-stu-id="1de68-115">If your transport provider does this, any other TNEF-enabled transport providers that follow this convention will be able to interoperate with it.</span></span>
    
5. <span data-ttu-id="1de68-116">Verwendung [ITnef: IUnknown](itnefiunknown.md) Schnittstellenmethoden, beschreibt die Positionen der e-Mail-Anlagen im Nachrichtentext Tags einfügen.</span><span class="sxs-lookup"><span data-stu-id="1de68-116">Use [ITnef : IUnknown](itnefiunknown.md) interface methods to insert tags describing the positions of message attachments in the message text.</span></span> 
    
6. <span data-ttu-id="1de68-117">Greifen Sie auf den markierten Nachrichtentext über [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) -Methoden, und senden Sie sie an die messaging-System.</span><span class="sxs-lookup"><span data-stu-id="1de68-117">Access the tagged message text through [IStream](http://msdn.microsoft.com/de-de/library/aa380034%28VS.85%29.aspx) methods, and send it to the messaging system.</span></span> 
    
 <span data-ttu-id="1de68-118">**Zum Abrufen von gekapselte Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="1de68-118">**To retrieve encapsulated properties**</span></span>
  
1. <span data-ttu-id="1de68-119">Schreiben von Eigenschaften in eine neue Nachricht, einschließlich Nachrichtentext für die markierte, die die gekapselten Eigenschaften enthält, die messaging-System unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1de68-119">Write the properties supported by the messaging system into a new message, including the tagged message text that contains the encapsulated properties.</span></span>
    
2. <span data-ttu-id="1de68-120">Decodiert den TNEF-Stream aus der entsprechenden Anlage.</span><span class="sxs-lookup"><span data-stu-id="1de68-120">Decode the TNEF stream from the proper attachment.</span></span>
    
3. <span data-ttu-id="1de68-121">Alle anderen Anlagen decodieren und in neue MAPI-Anlagen auf eine Nachricht zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="1de68-121">Decode any other attachments and write them to new MAPI attachments on a message.</span></span>
    
4. <span data-ttu-id="1de68-122">Öffnen Sie den TNEF-Stream für die Decodierung mit der Funktion [OpenTnefStreamEx](opentnefstreamex.md) .</span><span class="sxs-lookup"><span data-stu-id="1de68-122">Open the TNEF stream for decoding using the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="1de68-123">Verwenden Sie die [ITnef::ExtractProps](itnef-extractprops.md) -Methode zum Decodieren des TNEF-Streams und die gekapselten Eigenschaften in die neue Nachricht zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="1de68-123">Use the [ITnef::ExtractProps](itnef-extractprops.md) method to decode the TNEF stream and write the encapsulated properties into the new message.</span></span> <span data-ttu-id="1de68-124">Codierten Eigenschaften, die Duplikate der nonencoded Eigenschaften sind überschreibt die nonencoded Eigenschaften, wenn die codierten Eigenschaften decodiert werden.</span><span class="sxs-lookup"><span data-stu-id="1de68-124">Any encoded properties that are duplicates of nonencoded properties will overwrite the nonencoded properties when the encoded properties are decoded.</span></span> 
    
6. <span data-ttu-id="1de68-125">Verwenden Sie die [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) -Methode zum Analysieren des Nachrichtentext Anlage Positionen von Tags in den Nachrichtentext wiederhergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1de68-125">Use the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to parse the message text to recover attachment positions from the tags in the message text.</span></span> 
    

