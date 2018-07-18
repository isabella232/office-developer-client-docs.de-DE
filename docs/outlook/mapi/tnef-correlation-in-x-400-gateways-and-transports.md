---
title: TNEF-Korrelation in X.400-Gateways und Transport
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
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a>TNEF-Korrelation in X.400-Gateways und Transport

  
  
**Betrifft**: Outlook 
  
Gateways und Transport, die Verbindung von x. 400-basierte Systeme, verwenden Sie den Wert des Attributs IM_THIS_IPM x. 400- und das **AttMessageID** TNEF-Attribut TNEF Korrelation implementieren. 
  
Der Wert des Attributs IM_THIS_IPM der ausgehende Nachricht wird in **AttMessageID** im Datenstrom TNEF kopiert. Das IM_THIS_IPM x. 400-Attribut ist in der Regel eine Zeichenfolge zwar das **AttMessageID** TNEF-Attribut eine Zeichenfolge mit Hexadezimalzeichen, die einen Binärwert darstellt. Aus diesem Grund muss jedes Zeichen im IM_THIS_IPM x. 400-Attribut, einschließlich des abschließenden Null-Zeichens in 2 Zeichen hexadezimale Zeichenfolge, der den ASCII-Wert des Zeichens konvertiert werden soll. Beispielsweise, wenn das IM_THIS_IPM x. 400-Attribut die folgende Zeichenfolge: 
  
3030322D3030312D305337533A3A3936303631312D313533373030
  
der Wert der **AttMessageID** würde dann die folgende Sequenz von Hexadezimalzahlen entsprechen: 
  
33 30 33 30 33 32 32 44
  
33 30 33 30 33 31 32 44
  
33 30 35 33 33 37 35 33
  
33 41 33 41 33 39 33 36
  
33 30 33 36 33 31 33 31
  
32 44 33 31 33 35 33 33
  
33 37 33 30 33 30 00
  
Dieses Verfahren wird von Microsoft Exchange Server x. 400 Connector verwendet. Dieses Verfahren sollte verwendet werden, durch eine beliebige x. 400-Gateways und Transport, die Microsoft Exchange Server hergestellt werden, um die Interoperabilität zu maximieren soll.
  
Größte Kompatibilität mit Microsoft-Software sowohl geplante als auch vorhanden sollte das IM_THIS_IPM x. 400-Attribut auch der **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md))-Eigenschaft kopiert werden. Da **PR_TNEF_CORRELATION_KEY** eine binäre Eigenschaft ist, ist jedoch keine Übersetzung in eine hexadezimale Zeichenfolge erforderlich. 
  

