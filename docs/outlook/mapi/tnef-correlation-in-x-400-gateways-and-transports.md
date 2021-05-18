---
title: TNEF-Korrelation in X.400-Gateways und -Transporten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0ffa0802-bfdd-4993-b4a3-142e5d15bfb4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e08f16ff60a282f1be3adf93d858471e38d19957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406374"
---
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a>TNEF-Korrelation in X.400-Gateways und -Transporten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gateways und Transporte, die eine Verbindung mit X.400-basierten Systemen herstellen, verwenden den Wert des IM_THIS_IPM X.400-Attributs und des **attMessageID-TNEF-Attributs,** um die TNEF-Korrelation zu implementieren. 
  
Der Wert des IM_THIS_IPM der ausgehenden Nachricht wird in **attMessageID** im TNEF-Stream kopiert. Das IM_THIS_IPM X.400-Attribut ist in der Regel eine Zeichenfolge, während das **attMessageID-TNEF-Attribut** eine Zeichenfolge von hexadezimalen Ziffern ist, die einen binären Wert darstellen. Daher muss jedes Zeichen im IM_THIS_IPM X.400-Attribut, einschließlich des endenden Nullzeichens, in eine hexadezimale Zeichenfolge mit zwei Zeichen konvertiert werden, die den ASCII-Wert dieses Zeichens darstellt. Wenn beispielsweise das IM_THIS_IPM X.400-Attribut die folgende Zeichenfolge ist: 
  
3030322D3030312D305337533A3A3936303631312D313533373030
  
dann würde der Wert **von attMessageID** die folgende Sequenz von hexadezimalen Ziffern sein: 
  
33 30 33 30 33 32 32 44
  
33 30 33 30 33 31 32 44
  
33 30 35 33 33 37 35 33
  
33 41 33 41 33 39 33 36
  
33 30 33 36 33 31 33 31
  
32 44 33 31 33 35 33 33
  
33 37 33 30 33 30 00
  
Diese Technik wird vom X.400 Microsoft Exchange Server Verwendet. Diese Technik sollte von allen X.400-Gateways und -Transporten verwendet werden, die eine Verbindung mit Microsoft Exchange Server herstellen, um die Interoperabilität zu maximieren.
  
Um eine größtmögliche Kompatibilität mit zukünftiger und vorhandener #A0 zu gewährleisten, sollte das IM_THIS_IPM X.400-Attribut auch in die PR_TNEF_CORRELATION_KEY -[PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md) **-Eigenschaft** kopiert werden. Da PR_TNEF_CORRELATION_KEY **jedoch** eine binäre Eigenschaft ist, ist keine Übersetzung in eine hexadezimale Zeichenfolge erforderlich. 
  

