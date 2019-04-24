---
title: TNEF-Verarbeitung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d324fb3-d917-4502-b3a4-179c479deb79
description: 'Letzte �nderung: Donnerstag, 5. Juli 2012'
ms.openlocfilehash: 066ad3dfb64161e326b92fef7774d5b3b9461d8a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339599"
---
# <a name="tnef-processing"></a><span data-ttu-id="0676c-103">TNEF-Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="0676c-103">TNEF Processing</span></span>

  
  
<span data-ttu-id="0676c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0676c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0676c-105">In der folgenden Reihe von Aktionen wird beschrieben, wie mithilfe von TNEF-Methoden ausgehende und eingehende Nachrichten verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="0676c-105">The following series of actions describe how transports use TNEF methods to process outgoing and incoming messages.</span></span>
  
 <span data-ttu-id="0676c-106">**So senden Sie eine Nachricht mit einem TNEF-Datenstrom**</span><span class="sxs-lookup"><span data-stu-id="0676c-106">**To send a message that includes a TNEF stream**</span></span>
  
1. <span data-ttu-id="0676c-107">Verarbeiten Sie die Nachrichteneigenschaften, die vom Messagingsystem unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="0676c-107">Process the message properties that are supported by the messaging system.</span></span>
    
2. <span data-ttu-id="0676c-108">Markieren Sie die Nachricht in einer implementierungsspezifischen Weise, sodass der empfangende Transportanbieter bestimmen kann, dass die Nachricht die TNEF-Verarbeitung erfordert.</span><span class="sxs-lookup"><span data-stu-id="0676c-108">Mark the message in an implementation specific way so that the receiving transport provider can determine that the message requires TNEF processing.</span></span> <span data-ttu-id="0676c-109">Beispielsweise kann ein TNEF-Transportanbieter, der an ein SMTP-Messagingsystem sendet, ein benutzerdefiniertes Kopfzeilenfeld wie "X-CONTAINs-TNEF" hinzufügen, um anzugeben, dass die Nachricht TNEF-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="0676c-109">For example, a TNEF transport provider sending to an SMTP messaging system might add a custom header field like "X-CONTAINS-TNEF" to indicate that the message contains TNEF data.</span></span>
    
3. <span data-ttu-id="0676c-110">Rufen Sie ein TNEF-Objekt ab, und verwenden Sie es, um die vom Messagingsystem nicht unterstützten Nachrichteneigenschaften in einen TNEF-Datenstrom einzukapseln.</span><span class="sxs-lookup"><span data-stu-id="0676c-110">Obtain a TNEF object and use it to encapsulate the message properties not supported by the messaging system into a TNEF stream.</span></span>
    
4. <span data-ttu-id="0676c-111">Codieren Sie den TNEF-Stream mithilfe des Attachment-Modells des Messagingsystems.</span><span class="sxs-lookup"><span data-stu-id="0676c-111">Encode the TNEF stream using the messaging system's attachment model.</span></span> <span data-ttu-id="0676c-112">Wenn das zugrunde liegende Anlagenmodell beispielsweise UUEncode-Anlagen ist und diese an den Nachrichtentext angefügt wird, muss der TNEF-Stream vom Transportanbieter in eine andere Anlage eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0676c-112">For example, if the underlying attachment model is to uuencode attachments and append them to the message text, then the transport provider must uuencode the TNEF stream into another attachment.</span></span> <span data-ttu-id="0676c-113">Der Transportanbieter muss außerdem eine Methode implementieren, um zu erkennen, welche Anlage den codierten TNEF-Stream enthält, wenn er eine Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="0676c-113">The transport provider must also implement a method for recognizing which attachment contains the encoded TNEF stream when it receives a message.</span></span> <span data-ttu-id="0676c-114">Die Standardmethode zum Markieren dieser Anlage besteht darin, ihr einen Dateinamen "WINMAIL" zuzuweisen. DAT ".</span><span class="sxs-lookup"><span data-stu-id="0676c-114">The standard way to mark this attachment is to give it an attachment filename of "WINMAIL.DAT".</span></span> <span data-ttu-id="0676c-115">Wenn Ihr Transportanbieter dies tut, können alle anderen TNEF-fähigen Transportanbieter, die dieser Konvention folgen, mit dieser zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="0676c-115">If your transport provider does this, any other TNEF-enabled transport providers that follow this convention will be able to interoperate with it.</span></span>
    
5. <span data-ttu-id="0676c-116">Verwenden Sie [ITnef: IUnknown](itnefiunknown.md) -Schnittstellenmethoden, um Tags einzufügen, die die Positionen von Nachrichtenanlagen im Nachrichtentext beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0676c-116">Use [ITnef : IUnknown](itnefiunknown.md) interface methods to insert tags describing the positions of message attachments in the message text.</span></span> 
    
6. <span data-ttu-id="0676c-117">Zugreifen auf den markierten Nachrichtentext über [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Methoden und senden an das Messagingsystem.</span><span class="sxs-lookup"><span data-stu-id="0676c-117">Access the tagged message text through [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) methods, and send it to the messaging system.</span></span> 
    
 <span data-ttu-id="0676c-118">**So rufen Sie gekapselte Eigenschaften ab**</span><span class="sxs-lookup"><span data-stu-id="0676c-118">**To retrieve encapsulated properties**</span></span>
  
1. <span data-ttu-id="0676c-119">Schreiben Sie die vom Messagingsystem unterstützten Eigenschaften in eine neue Nachricht, einschließlich des markierten Nachrichtentexts, der die gekapselte Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="0676c-119">Write the properties supported by the messaging system into a new message, including the tagged message text that contains the encapsulated properties.</span></span>
    
2. <span data-ttu-id="0676c-120">DeCodieren Sie den TNEF-Datenstrom aus der richtigen Anlage.</span><span class="sxs-lookup"><span data-stu-id="0676c-120">Decode the TNEF stream from the proper attachment.</span></span>
    
3. <span data-ttu-id="0676c-121">DeCodieren Sie alle anderen Anlagen, und schreiben Sie Sie in neue MAPI-Anlagen in einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0676c-121">Decode any other attachments and write them to new MAPI attachments on a message.</span></span>
    
4. <span data-ttu-id="0676c-122">Öffnen Sie den TNEF-Stream zur Decodierung mithilfe der [OpenTnefStreamEx](opentnefstreamex.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="0676c-122">Open the TNEF stream for decoding using the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="0676c-123">Verwenden Sie die [ITnef:: ExtractProps](itnef-extractprops.md) -Methode, um den TNEF-Stream zu decodieren und die gekapselte Eigenschaften in die neue Nachricht zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="0676c-123">Use the [ITnef::ExtractProps](itnef-extractprops.md) method to decode the TNEF stream and write the encapsulated properties into the new message.</span></span> <span data-ttu-id="0676c-124">Alle codierten Eigenschaften, die Duplikate von nicht codierten Eigenschaften sind, überschreiben die nicht codierten Eigenschaften, wenn die codierten Eigenschaften decodiert werden.</span><span class="sxs-lookup"><span data-stu-id="0676c-124">Any encoded properties that are duplicates of nonencoded properties will overwrite the nonencoded properties when the encoded properties are decoded.</span></span> 
    
6. <span data-ttu-id="0676c-125">Verwenden Sie die [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) -Methode, um den Nachrichtentext zu analysieren, um die Anlagen Positionen der Tags im Nachrichtentext wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="0676c-125">Use the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to parse the message text to recover attachment positions from the tags in the message text.</span></span> 
    

