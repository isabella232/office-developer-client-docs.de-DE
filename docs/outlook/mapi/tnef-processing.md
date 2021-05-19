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
# <a name="tnef-processing"></a>TNEF-Verarbeitung

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
In der folgenden Aktionsreihe wird beschrieben, wie Transporte TNEF-Methoden verwenden, um ausgehende und eingehende Nachrichten zu verarbeiten.
  
 **So senden Sie eine Nachricht, die einen TNEF-Stream enthält**
  
1. Verarbeiten Sie die Nachrichteneigenschaften, die vom Messagingsystem unterstützt werden.
    
2. Markieren Sie die Nachricht auf eine implementierungsspezifische Weise, damit der empfangende Transportanbieter feststellen kann, dass für die Nachricht eine TNEF-Verarbeitung erforderlich ist. Beispielsweise kann ein TNEF-Transportanbieter, der an ein SMTP-Messagingsystem sendet, ein benutzerdefiniertes Kopfzeilenfeld wie "X-CONTAINS-TNEF" hinzufügen, um anzugeben, dass die Nachricht TNEF-Daten enthält.
    
3. Rufen Sie ein TNEF-Objekt ab, und verwenden Sie es, um die Nachrichteneigenschaften zu kapseln, die vom Messagingsystem nicht unterstützt werden, in einen TNEF-Stream.
    
4. Codieren Sie den TNEF-Stream mithilfe des Anlagenmodells des Messagingsystems. Wenn das zugrunde liegende Anlagenmodell beispielsweise anlagen codieren und an den Nachrichtentext anfügen soll, muss der Transportanbieter den TNEF-Datenstrom in eine andere Anlage uuencodieren. Der Transportanbieter muss auch eine Methode implementieren, um zu erkennen, welche Anlage den codierten TNEF-Stream enthält, wenn er eine Nachricht empfängt. Die standardmäßige Möglichkeit, diese Anlage zu markieren, ist, ihr den Anlagendateinamen "WINMAIL" zu geben. DAT". Wenn Ihr Transportanbieter dies tut, können alle anderen TNEF-aktivierten Transportanbieter, die dieser Konvention folgen, mit ihm zusammenarbeiten.
    
5. Verwenden [Sie ITnef : IUnknown-Schnittstellenmethoden](itnefiunknown.md) zum Einfügen von Tags, die die Positionen von Nachrichtenanlagen im Nachrichtentext beschreiben. 
    
6. Greifen Sie über [IStream-Methoden](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) auf den markierten Nachrichtentext zu, und senden Sie ihn an das Messagingsystem. 
    
 **So rufen Sie gekapselte Eigenschaften ab**
  
1. Schreiben Sie die vom Messagingsystem unterstützten Eigenschaften in eine neue Nachricht, einschließlich des markierten Nachrichtentexts, der die gekapselten Eigenschaften enthält.
    
2. Decodieren Sie den TNEF-Stream aus der richtigen Anlage.
    
3. Decodieren Sie alle anderen Anlagen, und schreiben Sie sie in neue MAPI-Anlagen in einer Nachricht.
    
4. Öffnen Sie den TNEF-Stream zum Decodieren mithilfe der [OpenTnefStreamEx-Funktion.](opentnefstreamex.md) 
    
5. Verwenden Sie [die ITnef::ExtractProps-Methode,](itnef-extractprops.md) um den TNEF-Stream zu decodieren und die gekapselten Eigenschaften in die neue Nachricht zu schreiben. Alle codierten Eigenschaften, die Duplikate nicht codierter Eigenschaften sind, überschreiben die nicht codierten Eigenschaften, wenn die codierten Eigenschaften decodiert werden. 
    
6. Verwenden Sie [die ITnef::OpenTaggedBody-Methode,](itnef-opentaggedbody.md) um den Nachrichtentext zu analysieren, um Anlagenpositionen aus den Tags im Nachrichtentext wiederhergestellt zu werden. 
    

