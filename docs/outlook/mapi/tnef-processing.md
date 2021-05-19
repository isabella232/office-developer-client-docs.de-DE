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
# <a name="tnef-processing"></a><span data-ttu-id="69804-103">TNEF-Verarbeitung</span><span class="sxs-lookup"><span data-stu-id="69804-103">TNEF Processing</span></span>

  
  
<span data-ttu-id="69804-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69804-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69804-105">In der folgenden Aktionsreihe wird beschrieben, wie Transporte TNEF-Methoden verwenden, um ausgehende und eingehende Nachrichten zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="69804-105">The following series of actions describe how transports use TNEF methods to process outgoing and incoming messages.</span></span>
  
 <span data-ttu-id="69804-106">**So senden Sie eine Nachricht, die einen TNEF-Stream enthält**</span><span class="sxs-lookup"><span data-stu-id="69804-106">**To send a message that includes a TNEF stream**</span></span>
  
1. <span data-ttu-id="69804-107">Verarbeiten Sie die Nachrichteneigenschaften, die vom Messagingsystem unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="69804-107">Process the message properties that are supported by the messaging system.</span></span>
    
2. <span data-ttu-id="69804-108">Markieren Sie die Nachricht auf eine implementierungsspezifische Weise, damit der empfangende Transportanbieter feststellen kann, dass für die Nachricht eine TNEF-Verarbeitung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="69804-108">Mark the message in an implementation specific way so that the receiving transport provider can determine that the message requires TNEF processing.</span></span> <span data-ttu-id="69804-109">Beispielsweise kann ein TNEF-Transportanbieter, der an ein SMTP-Messagingsystem sendet, ein benutzerdefiniertes Kopfzeilenfeld wie "X-CONTAINS-TNEF" hinzufügen, um anzugeben, dass die Nachricht TNEF-Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="69804-109">For example, a TNEF transport provider sending to an SMTP messaging system might add a custom header field like "X-CONTAINS-TNEF" to indicate that the message contains TNEF data.</span></span>
    
3. <span data-ttu-id="69804-110">Rufen Sie ein TNEF-Objekt ab, und verwenden Sie es, um die Nachrichteneigenschaften zu kapseln, die vom Messagingsystem nicht unterstützt werden, in einen TNEF-Stream.</span><span class="sxs-lookup"><span data-stu-id="69804-110">Obtain a TNEF object and use it to encapsulate the message properties not supported by the messaging system into a TNEF stream.</span></span>
    
4. <span data-ttu-id="69804-111">Codieren Sie den TNEF-Stream mithilfe des Anlagenmodells des Messagingsystems.</span><span class="sxs-lookup"><span data-stu-id="69804-111">Encode the TNEF stream using the messaging system's attachment model.</span></span> <span data-ttu-id="69804-112">Wenn das zugrunde liegende Anlagenmodell beispielsweise anlagen codieren und an den Nachrichtentext anfügen soll, muss der Transportanbieter den TNEF-Datenstrom in eine andere Anlage uuencodieren.</span><span class="sxs-lookup"><span data-stu-id="69804-112">For example, if the underlying attachment model is to uuencode attachments and append them to the message text, then the transport provider must uuencode the TNEF stream into another attachment.</span></span> <span data-ttu-id="69804-113">Der Transportanbieter muss auch eine Methode implementieren, um zu erkennen, welche Anlage den codierten TNEF-Stream enthält, wenn er eine Nachricht empfängt.</span><span class="sxs-lookup"><span data-stu-id="69804-113">The transport provider must also implement a method for recognizing which attachment contains the encoded TNEF stream when it receives a message.</span></span> <span data-ttu-id="69804-114">Die standardmäßige Möglichkeit, diese Anlage zu markieren, ist, ihr den Anlagendateinamen "WINMAIL" zu geben. DAT".</span><span class="sxs-lookup"><span data-stu-id="69804-114">The standard way to mark this attachment is to give it an attachment filename of "WINMAIL.DAT".</span></span> <span data-ttu-id="69804-115">Wenn Ihr Transportanbieter dies tut, können alle anderen TNEF-aktivierten Transportanbieter, die dieser Konvention folgen, mit ihm zusammenarbeiten.</span><span class="sxs-lookup"><span data-stu-id="69804-115">If your transport provider does this, any other TNEF-enabled transport providers that follow this convention will be able to interoperate with it.</span></span>
    
5. <span data-ttu-id="69804-116">Verwenden [Sie ITnef : IUnknown-Schnittstellenmethoden](itnefiunknown.md) zum Einfügen von Tags, die die Positionen von Nachrichtenanlagen im Nachrichtentext beschreiben.</span><span class="sxs-lookup"><span data-stu-id="69804-116">Use [ITnef : IUnknown](itnefiunknown.md) interface methods to insert tags describing the positions of message attachments in the message text.</span></span> 
    
6. <span data-ttu-id="69804-117">Greifen Sie über [IStream-Methoden](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) auf den markierten Nachrichtentext zu, und senden Sie ihn an das Messagingsystem.</span><span class="sxs-lookup"><span data-stu-id="69804-117">Access the tagged message text through [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) methods, and send it to the messaging system.</span></span> 
    
 <span data-ttu-id="69804-118">**So rufen Sie gekapselte Eigenschaften ab**</span><span class="sxs-lookup"><span data-stu-id="69804-118">**To retrieve encapsulated properties**</span></span>
  
1. <span data-ttu-id="69804-119">Schreiben Sie die vom Messagingsystem unterstützten Eigenschaften in eine neue Nachricht, einschließlich des markierten Nachrichtentexts, der die gekapselten Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="69804-119">Write the properties supported by the messaging system into a new message, including the tagged message text that contains the encapsulated properties.</span></span>
    
2. <span data-ttu-id="69804-120">Decodieren Sie den TNEF-Stream aus der richtigen Anlage.</span><span class="sxs-lookup"><span data-stu-id="69804-120">Decode the TNEF stream from the proper attachment.</span></span>
    
3. <span data-ttu-id="69804-121">Decodieren Sie alle anderen Anlagen, und schreiben Sie sie in neue MAPI-Anlagen in einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="69804-121">Decode any other attachments and write them to new MAPI attachments on a message.</span></span>
    
4. <span data-ttu-id="69804-122">Öffnen Sie den TNEF-Stream zum Decodieren mithilfe der [OpenTnefStreamEx-Funktion.](opentnefstreamex.md)</span><span class="sxs-lookup"><span data-stu-id="69804-122">Open the TNEF stream for decoding using the [OpenTnefStreamEx](opentnefstreamex.md) function.</span></span> 
    
5. <span data-ttu-id="69804-123">Verwenden Sie [die ITnef::ExtractProps-Methode,](itnef-extractprops.md) um den TNEF-Stream zu decodieren und die gekapselten Eigenschaften in die neue Nachricht zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="69804-123">Use the [ITnef::ExtractProps](itnef-extractprops.md) method to decode the TNEF stream and write the encapsulated properties into the new message.</span></span> <span data-ttu-id="69804-124">Alle codierten Eigenschaften, die Duplikate nicht codierter Eigenschaften sind, überschreiben die nicht codierten Eigenschaften, wenn die codierten Eigenschaften decodiert werden.</span><span class="sxs-lookup"><span data-stu-id="69804-124">Any encoded properties that are duplicates of nonencoded properties will overwrite the nonencoded properties when the encoded properties are decoded.</span></span> 
    
6. <span data-ttu-id="69804-125">Verwenden Sie [die ITnef::OpenTaggedBody-Methode,](itnef-opentaggedbody.md) um den Nachrichtentext zu analysieren, um Anlagenpositionen aus den Tags im Nachrichtentext wiederhergestellt zu werden.</span><span class="sxs-lookup"><span data-stu-id="69804-125">Use the [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) method to parse the message text to recover attachment positions from the tags in the message text.</span></span> 
    

