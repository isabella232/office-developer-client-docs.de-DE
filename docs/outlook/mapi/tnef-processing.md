---
title: TNEF-Verarbeitung
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 4d324fb3-d917-4502-b3a4-179c479deb79
description: 'Letzte �nderung: Donnerstag, 5. Juli 2012'
ms.openlocfilehash: 7e194d5c23a092ee239d4efa3dad47b7dadb732c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59624041"
---
# <a name="tnef-processing"></a>TNEF-Verarbeitung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In der folgenden Aktionsreihe wird beschrieben, wie transports TNEF-Methoden verwenden, um ausgehende und eingehende Nachrichten zu verarbeiten.
  
 **So senden Sie eine Nachricht, die einen TNEF-Stream enthält**
  
1. Verarbeiten der Nachrichteneigenschaften, die vom Messagingsystem unterstützt werden.
    
2. Markieren Sie die Nachricht auf implementierungsspezifische Weise, damit der empfangende Transportanbieter feststellen kann, dass die Nachricht eine TNEF-Verarbeitung erfordert. Beispielsweise kann ein TNEF-Transportanbieter, der an ein SMTP-Messagingsystem sendet, ein benutzerdefiniertes Kopfzeilenfeld wie "X-CONTAINS-TNEF" hinzufügen, um anzugeben, dass die Nachricht TNEF-Daten enthält.
    
3. Rufen Sie ein TNEF-Objekt ab, und verwenden Sie es zum Kapseln der Nachrichteneigenschaften, die vom Messagingsystem nicht unterstützt werden, in einen TNEF-Stream.
    
4. Codieren Sie den TNEF-Datenstrom mithilfe des Anlagenmodells des Messagingsystems. Wenn das zugrunde liegende Anlagenmodell z. B. das Uuencode von Anlagen und das Anfügen an den Nachrichtentext ist, muss der Transportanbieter den TNEF-Datenstrom in eine andere Anlage codieren. Der Transportanbieter muss auch eine Methode zum Erkennen der Anlage implementieren, die den codierten TNEF-Stream enthält, wenn er eine Nachricht empfängt. Die Standardmethode zum Markieren dieser Anlage besteht darin, der Anlage den Dateinamen "WINMAIL" zu geben. DAT". Wenn ihr Transportanbieter dies tut, können alle anderen TNEF-fähigen Transportanbieter, die dieser Konvention folgen, mit ihm zusammenarbeiten.
    
5. Verwenden Sie [ITnef : IUnknown-Schnittstellenmethoden,](itnefiunknown.md) um Tags einzufügen, die die Position von Nachrichtenanlagen im Nachrichtentext beschreiben. 
    
6. Greifen Sie über [IStream-Methoden](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) auf den markierten Nachrichtentext zu, und senden Sie ihn an das Messagingsystem. 
    
 **So rufen Sie gekapselte Eigenschaften ab**
  
1. Schreiben Sie die vom Messagingsystem unterstützten Eigenschaften in eine neue Nachricht, einschließlich des markierten Nachrichtentexts, der die gekapselten Eigenschaften enthält.
    
2. Decodieren Sie den TNEF-Stream aus der richtigen Anlage.
    
3. Decodieren Sie alle anderen Anlagen, und schreiben Sie sie in neue MAPI-Anlagen in einer Nachricht.
    
4. Öffnen Sie den TNEF-Stream für die Decodierung mithilfe der [OpenTnefStreamEx-Funktion.](opentnefstreamex.md) 
    
5. Verwenden Sie die [ITnef::ExtractProps-Methode,](itnef-extractprops.md) um den TNEF-Stream zu decodieren und die gekapselten Eigenschaften in die neue Nachricht zu schreiben. Alle codierten Eigenschaften, die Duplikate nicht codierter Eigenschaften sind, überschreiben die nicht codierten Eigenschaften, wenn die codierten Eigenschaften decodiert werden. 
    
6. Verwenden Sie die [ITnef::OpenTaggedBody-Methode,](itnef-opentaggedbody.md) um den Nachrichtentext zu analysieren, um Anlagenpositionen aus den Tags im Nachrichtentext wiederherzustellen. 
    

