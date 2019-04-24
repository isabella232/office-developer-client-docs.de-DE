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
  
In der folgenden Reihe von Aktionen wird beschrieben, wie mithilfe von TNEF-Methoden ausgehende und eingehende Nachrichten verarbeitet werden.
  
 **So senden Sie eine Nachricht mit einem TNEF-Datenstrom**
  
1. Verarbeiten Sie die Nachrichteneigenschaften, die vom Messagingsystem unterstützt werden.
    
2. Markieren Sie die Nachricht in einer implementierungsspezifischen Weise, sodass der empfangende Transportanbieter bestimmen kann, dass die Nachricht die TNEF-Verarbeitung erfordert. Beispielsweise kann ein TNEF-Transportanbieter, der an ein SMTP-Messagingsystem sendet, ein benutzerdefiniertes Kopfzeilenfeld wie "X-CONTAINs-TNEF" hinzufügen, um anzugeben, dass die Nachricht TNEF-Daten enthält.
    
3. Rufen Sie ein TNEF-Objekt ab, und verwenden Sie es, um die vom Messagingsystem nicht unterstützten Nachrichteneigenschaften in einen TNEF-Datenstrom einzukapseln.
    
4. Codieren Sie den TNEF-Stream mithilfe des Attachment-Modells des Messagingsystems. Wenn das zugrunde liegende Anlagenmodell beispielsweise UUEncode-Anlagen ist und diese an den Nachrichtentext angefügt wird, muss der TNEF-Stream vom Transportanbieter in eine andere Anlage eingefügt werden. Der Transportanbieter muss außerdem eine Methode implementieren, um zu erkennen, welche Anlage den codierten TNEF-Stream enthält, wenn er eine Nachricht empfängt. Die Standardmethode zum Markieren dieser Anlage besteht darin, ihr einen Dateinamen "WINMAIL" zuzuweisen. DAT ". Wenn Ihr Transportanbieter dies tut, können alle anderen TNEF-fähigen Transportanbieter, die dieser Konvention folgen, mit dieser zusammenarbeiten.
    
5. Verwenden Sie [ITnef: IUnknown](itnefiunknown.md) -Schnittstellenmethoden, um Tags einzufügen, die die Positionen von Nachrichtenanlagen im Nachrichtentext beschreiben. 
    
6. Zugreifen auf den markierten Nachrichtentext über [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) -Methoden und senden an das Messagingsystem. 
    
 **So rufen Sie gekapselte Eigenschaften ab**
  
1. Schreiben Sie die vom Messagingsystem unterstützten Eigenschaften in eine neue Nachricht, einschließlich des markierten Nachrichtentexts, der die gekapselte Eigenschaften enthält.
    
2. DeCodieren Sie den TNEF-Datenstrom aus der richtigen Anlage.
    
3. DeCodieren Sie alle anderen Anlagen, und schreiben Sie Sie in neue MAPI-Anlagen in einer Nachricht.
    
4. Öffnen Sie den TNEF-Stream zur Decodierung mithilfe der [OpenTnefStreamEx](opentnefstreamex.md) -Funktion. 
    
5. Verwenden Sie die [ITnef:: ExtractProps](itnef-extractprops.md) -Methode, um den TNEF-Stream zu decodieren und die gekapselte Eigenschaften in die neue Nachricht zu schreiben. Alle codierten Eigenschaften, die Duplikate von nicht codierten Eigenschaften sind, überschreiben die nicht codierten Eigenschaften, wenn die codierten Eigenschaften decodiert werden. 
    
6. Verwenden Sie die [ITnef:: OpenTaggedBody](itnef-opentaggedbody.md) -Methode, um den Nachrichtentext zu analysieren, um die Anlagen Positionen der Tags im Nachrichtentext wiederherzustellen. 
    

