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
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a>TNEF-Korrelation in X. 400-Gateways und-Übertragungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gateways und Übertragungen, die mit X. 400-basierten Systemen verbunden sind, verwenden Sie den Wert des IM_THIS_IPM X. 400-Attributs und das **attMessageID** TNEF-Attribut, um die TNEF-Korrelation zu implementieren. 
  
Der Wert des IM_THIS_IPM-Attributs der ausgehenden Nachricht wird in **attMessageID** im TNEF-Stream kopiert. Das IM_THIS_IPM X. 400-Attribut ist in der Regel eine Zeichenfolge, das **attMessageID** -TNEF-Attribut ist eine Zeichenfolge mit Hexadezimalziffern, die einen Binärwert darstellt. Daher muss jedes Zeichen im IM_THIS_IPM X. 400-Attribut, einschließlich des abschließenden NULL-Zeichens, in eine hexadezimale Zeichenfolge mit zwei Zeichen konvertiert werden, die den ASCII-Wert dieses Zeichens darstellt. Wenn das IM_THIS_IPM-Attribut X. 400 beispielsweise die folgende Zeichenfolge ist: 
  
3030322D3030312D305337533A3A3936303631312D313533373030
  
dann wäre der Wert von **attMessageID** die folgende Sequenz von Hexadezimalziffern: 
  
33 30 33 30 33 32 32 44
  
33 30 33 30 33 31 32 44
  
33 30 35 33 33 37 35 33
  
33 41 33 41 33 39 33 36
  
33 30 33 36 33 31 33 31
  
32 44 33 31 33 35 33 33
  
33 37 33 30 33 30 00
  
Diese Technik wird vom Microsoft Exchange Server X. 400-Connector verwendet. Diese Technik sollte von allen X. 400-Gateways und-Übertragungen verwendet werden, die eine Verbindung mit Microsoft Exchange Server herstellen, um die Interoperabilität zu maximieren.
  
Für größtmögliche Kompatibilität mit der zukünftigen und der aktuellen Microsoft-Software sollte auch das IM_THIS_IPM X. 400-Attribut in die **PR_TNEF_CORRELATION_KEY** ([pidtagtnefcorrelationkey (](pidtagtnefcorrelationkey-canonical-property.md))-Eigenschaft kopiert werden. Da **PR_TNEF_CORRELATION_KEY** eine binäre Eigenschaft ist, ist jedoch keine Übersetzung in eine Hexadezimalzeichenfolge erforderlich. 
  

