---
title: TNEF-Korrelation in X. 400-Gateways und-Übertragungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0ffa0802-bfdd-4993-b4a3-142e5d15bfb4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e08f16ff60a282f1be3adf93d858471e38d19957
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339627"
---
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a><span data-ttu-id="a1573-103">TNEF-Korrelation in X. 400-Gateways und-Übertragungen</span><span class="sxs-lookup"><span data-stu-id="a1573-103">TNEF Correlation in X.400 Gateways and Transports</span></span>

  
  
<span data-ttu-id="a1573-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1573-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1573-105">Gateways und Übertragungen, die mit X. 400-basierten Systemen verbunden sind, verwenden Sie den Wert des IM_THIS_IPM X. 400-Attributs und das **attMessageID** TNEF-Attribut, um die TNEF-Korrelation zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="a1573-105">Gateways and transports that connect to X.400-based systems, use the value of the IM_THIS_IPM X.400 attribute and the **attMessageID** TNEF attribute to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="a1573-106">Der Wert des IM_THIS_IPM-Attributs der ausgehenden Nachricht wird in **attMessageID** im TNEF-Stream kopiert.</span><span class="sxs-lookup"><span data-stu-id="a1573-106">The value of the IM_THIS_IPM attribute of the outbound message is copied to **attMessageID** in the TNEF stream.</span></span> <span data-ttu-id="a1573-107">Das IM_THIS_IPM X. 400-Attribut ist in der Regel eine Zeichenfolge, das **attMessageID** -TNEF-Attribut ist eine Zeichenfolge mit Hexadezimalziffern, die einen Binärwert darstellt.</span><span class="sxs-lookup"><span data-stu-id="a1573-107">The IM_THIS_IPM X.400 attribute is typically a string, while the **attMessageID** TNEF attribute is a string of hexadecimal digits representing a binary value.</span></span> <span data-ttu-id="a1573-108">Daher muss jedes Zeichen im IM_THIS_IPM X. 400-Attribut, einschließlich des abschließenden NULL-Zeichens, in eine hexadezimale Zeichenfolge mit zwei Zeichen konvertiert werden, die den ASCII-Wert dieses Zeichens darstellt.</span><span class="sxs-lookup"><span data-stu-id="a1573-108">Therefore, each character in the IM_THIS_IPM X.400 attribute, including the terminating null character, must be converted to a 2-character hexadecimal string representing the ASCII value of that character.</span></span> <span data-ttu-id="a1573-109">Wenn das IM_THIS_IPM-Attribut X. 400 beispielsweise die folgende Zeichenfolge ist:</span><span class="sxs-lookup"><span data-stu-id="a1573-109">For instance, if the IM_THIS_IPM X.400 attribute is the following string:</span></span> 
  
<span data-ttu-id="a1573-110">3030322D3030312D305337533A3A3936303631312D313533373030</span><span class="sxs-lookup"><span data-stu-id="a1573-110">3030322D3030312D305337533A3A3936303631312D313533373030</span></span>
  
<span data-ttu-id="a1573-111">dann wäre der Wert von **attMessageID** die folgende Sequenz von Hexadezimalziffern:</span><span class="sxs-lookup"><span data-stu-id="a1573-111">then the value of **attMessageID** would be the following sequence of hexadecimal digits:</span></span> 
  
<span data-ttu-id="a1573-112">33 30 33 30 33 32 32 44</span><span class="sxs-lookup"><span data-stu-id="a1573-112">33 30 33 30 33 32 32 44</span></span>
  
<span data-ttu-id="a1573-113">33 30 33 30 33 31 32 44</span><span class="sxs-lookup"><span data-stu-id="a1573-113">33 30 33 30 33 31 32 44</span></span>
  
<span data-ttu-id="a1573-114">33 30 35 33 33 37 35 33</span><span class="sxs-lookup"><span data-stu-id="a1573-114">33 30 35 33 33 37 35 33</span></span>
  
<span data-ttu-id="a1573-115">33 41 33 41 33 39 33 36</span><span class="sxs-lookup"><span data-stu-id="a1573-115">33 41 33 41 33 39 33 36</span></span>
  
<span data-ttu-id="a1573-116">33 30 33 36 33 31 33 31</span><span class="sxs-lookup"><span data-stu-id="a1573-116">33 30 33 36 33 31 33 31</span></span>
  
<span data-ttu-id="a1573-117">32 44 33 31 33 35 33 33</span><span class="sxs-lookup"><span data-stu-id="a1573-117">32 44 33 31 33 35 33 33</span></span>
  
<span data-ttu-id="a1573-118">33 37 33 30 33 30 00</span><span class="sxs-lookup"><span data-stu-id="a1573-118">33 37 33 30 33 30 00</span></span>
  
<span data-ttu-id="a1573-119">Diese Technik wird vom Microsoft Exchange Server X. 400-Connector verwendet.</span><span class="sxs-lookup"><span data-stu-id="a1573-119">This technique is used by the Microsoft Exchange Server X.400 Connector.</span></span> <span data-ttu-id="a1573-120">Diese Technik sollte von allen X. 400-Gateways und-Übertragungen verwendet werden, die eine Verbindung mit Microsoft Exchange Server herstellen, um die Interoperabilität zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="a1573-120">This technique should be used by any X.400 gateways and transports that connect to Microsoft Exchange Server in order to maximize interoperability.</span></span>
  
<span data-ttu-id="a1573-121">Für größtmögliche Kompatibilität mit der zukünftigen und der aktuellen Microsoft-Software sollte auch das IM_THIS_IPM X. 400-Attribut in die **PR_TNEF_CORRELATION_KEY** ([pidtagtnefcorrelationkey (](pidtagtnefcorrelationkey-canonical-property.md))-Eigenschaft kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="a1573-121">For greatest compatibility with future as well as present Microsoft software, the IM_THIS_IPM X.400 attribute should also be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property.</span></span> <span data-ttu-id="a1573-122">Da **PR_TNEF_CORRELATION_KEY** eine binäre Eigenschaft ist, ist jedoch keine Übersetzung in eine Hexadezimalzeichenfolge erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a1573-122">However, since **PR_TNEF_CORRELATION_KEY** is a binary property, no translation into a hexadecimal string is necessary.</span></span> 
  

