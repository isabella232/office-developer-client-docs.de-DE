---
title: TNEF Korrelation x. 400-Gateways und Transport
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0ffa0802-bfdd-4993-b4a3-142e5d15bfb4
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ea5ca41ef21c72377ade72370e0aee1b313c92d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795733"
---
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a><span data-ttu-id="04e89-103">TNEF Korrelation x. 400-Gateways und Transport</span><span class="sxs-lookup"><span data-stu-id="04e89-103">TNEF Correlation in X.400 Gateways and Transports</span></span>

  
  
<span data-ttu-id="04e89-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="04e89-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="04e89-105">Gateways und Transport, die Verbindung von x. 400-basierte Systeme, verwenden Sie den Wert des Attributs IM_THIS_IPM x. 400- und das **AttMessageID** TNEF-Attribut TNEF Korrelation implementieren.</span><span class="sxs-lookup"><span data-stu-id="04e89-105">Gateways and transports that connect to X.400-based systems, use the value of the IM_THIS_IPM X.400 attribute and the **attMessageID** TNEF attribute to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="04e89-106">Der Wert des Attributs IM_THIS_IPM der ausgehende Nachricht wird in **AttMessageID** im Datenstrom TNEF kopiert.</span><span class="sxs-lookup"><span data-stu-id="04e89-106">The value of the IM_THIS_IPM attribute of the outbound message is copied to **attMessageID** in the TNEF stream.</span></span> <span data-ttu-id="04e89-107">Das IM_THIS_IPM x. 400-Attribut ist in der Regel eine Zeichenfolge zwar das **AttMessageID** TNEF-Attribut eine Zeichenfolge mit Hexadezimalzeichen, die einen Binärwert darstellt.</span><span class="sxs-lookup"><span data-stu-id="04e89-107">The IM_THIS_IPM X.400 attribute is typically a string, while the **attMessageID** TNEF attribute is a string of hexadecimal digits representing a binary value.</span></span> <span data-ttu-id="04e89-108">Aus diesem Grund muss jedes Zeichen im IM_THIS_IPM x. 400-Attribut, einschließlich des abschließenden Null-Zeichens in 2 Zeichen hexadezimale Zeichenfolge, der den ASCII-Wert des Zeichens konvertiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="04e89-108">Therefore, each character in the IM_THIS_IPM X.400 attribute, including the terminating null character, must be converted to a 2-character hexadecimal string representing the ASCII value of that character.</span></span> <span data-ttu-id="04e89-109">Beispielsweise, wenn das IM_THIS_IPM x. 400-Attribut die folgende Zeichenfolge:</span><span class="sxs-lookup"><span data-stu-id="04e89-109">For instance, if the IM_THIS_IPM X.400 attribute is the following string:</span></span> 
  
<span data-ttu-id="04e89-110">3030322D3030312D305337533A3A3936303631312D313533373030</span><span class="sxs-lookup"><span data-stu-id="04e89-110">3030322D3030312D305337533A3A3936303631312D313533373030</span></span>
  
<span data-ttu-id="04e89-111">der Wert der **AttMessageID** würde dann die folgende Sequenz von Hexadezimalzahlen entsprechen:</span><span class="sxs-lookup"><span data-stu-id="04e89-111">then the value of **attMessageID** would be the following sequence of hexadecimal digits:</span></span> 
  
<span data-ttu-id="04e89-112">33 30 33 30 33 32 32 44</span><span class="sxs-lookup"><span data-stu-id="04e89-112">33 30 33 30 33 32 32 44</span></span>
  
<span data-ttu-id="04e89-113">33 30 33 30 33 31 32 44</span><span class="sxs-lookup"><span data-stu-id="04e89-113">33 30 33 30 33 31 32 44</span></span>
  
<span data-ttu-id="04e89-114">33 30 35 33 33 37 35 33</span><span class="sxs-lookup"><span data-stu-id="04e89-114">33 30 35 33 33 37 35 33</span></span>
  
<span data-ttu-id="04e89-115">33 41 33 41 33 39 33 36</span><span class="sxs-lookup"><span data-stu-id="04e89-115">33 41 33 41 33 39 33 36</span></span>
  
<span data-ttu-id="04e89-116">33 30 33 36 33 31 33 31</span><span class="sxs-lookup"><span data-stu-id="04e89-116">33 30 33 36 33 31 33 31</span></span>
  
<span data-ttu-id="04e89-117">32 44 33 31 33 35 33 33</span><span class="sxs-lookup"><span data-stu-id="04e89-117">32 44 33 31 33 35 33 33</span></span>
  
<span data-ttu-id="04e89-118">33 37 33 30 33 30 00</span><span class="sxs-lookup"><span data-stu-id="04e89-118">33 37 33 30 33 30 00</span></span>
  
<span data-ttu-id="04e89-119">Dieses Verfahren wird von Microsoft Exchange Server x. 400 Connector verwendet.</span><span class="sxs-lookup"><span data-stu-id="04e89-119">This technique is used by the Microsoft Exchange Server X.400 Connector.</span></span> <span data-ttu-id="04e89-120">Dieses Verfahren sollte verwendet werden, durch eine beliebige x. 400-Gateways und Transport, die Microsoft Exchange Server hergestellt werden, um die Interoperabilität zu maximieren soll.</span><span class="sxs-lookup"><span data-stu-id="04e89-120">This technique should be used by any X.400 gateways and transports that connect to Microsoft Exchange Server in order to maximize interoperability.</span></span>
  
<span data-ttu-id="04e89-121">Größte Kompatibilität mit Microsoft-Software sowohl geplante als auch vorhanden sollte das IM_THIS_IPM x. 400-Attribut auch der **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))-Eigenschaft kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="04e89-121">For greatest compatibility with future as well as present Microsoft software, the IM_THIS_IPM X.400 attribute should also be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property.</span></span> <span data-ttu-id="04e89-122">Da **PR_TNEF_CORRELATION_KEY** eine binäre Eigenschaft ist, ist jedoch keine Übersetzung in eine hexadezimale Zeichenfolge erforderlich.</span><span class="sxs-lookup"><span data-stu-id="04e89-122">However, since **PR_TNEF_CORRELATION_KEY** is a binary property, no translation into a hexadecimal string is necessary.</span></span> 
  

