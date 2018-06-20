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
ms.openlocfilehash: bd9cc49f5d1d865d5d6b222677df0dd62ec36fd6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795732"
---
# <a name="tnef-processing"></a>TNEF-Verarbeitung

  
  
**Betrifft**: Outlook 
  
Die folgende Reihe von Aktionen wird beschrieben, wie Transporten TNEF-Methoden zum Verarbeiten von eingehender und ausgehender Nachrichten verwenden.
  
 **Senden eine Nachricht, die einen TNEF-Stream enthält**
  
1. Verarbeiten von den Eigenschaften der Nachricht, die von der messaging-System unterstützt werden.
    
2. Markieren Sie die Nachricht in einer Implementierung bestimmte Weise, damit der empfangenden Adressbuchhierarchie ermitteln kann, dass die Nachricht TNEF-Verarbeitung erforderlich ist. Eine TNEF-Transportdienst senden an eine SMTP-messaging-System möglicherweise beispielsweise ein benutzerdefinierter Header-Feld wie "X-enthält-TNEF" um anzugeben, dass die Nachricht TNEF-Daten enthält hinzufügen.
    
3. Abrufen eines TNEF-Objekts, und verwenden Sie es zum Kapseln der Nachrichteneigenschaften von messaging-System in einem Stream TNEF nicht unterstützt.
    
4. Codieren Sie mit der messaging-System Anlage Objektmodell TNEF-Stream. Beispielsweise wenn das zugrunde liegende Anlage Modell Uuencode Anlagen und den Nachrichtentext anfügen, muss dann der Adressbuchhierarchie Uuencode TNEF-Stream in einer anderen Anlage. Der Transportdienst muss auch eine Methode für die Erkennung von welche Anlage den codierten TNEF-Stream enthält, wenn sie eine Nachricht empfängt implementieren. Standardverfahren zum Kennzeichnen dieser Anlage ist, damit es erhält ein Dateiname der Anlage von "WINMAIL. FILTERN". Wenn der Adressbuchhierarchie dies der Fall ist, werden können mit ihm interagieren alle Transportanbieter TNEF-aktiviert, die dieser Konvention.
    
5. Verwendung [ITnef: IUnknown](itnefiunknown.md) Schnittstellenmethoden, beschreibt die Positionen der e-Mail-Anlagen im Nachrichtentext Tags einfügen. 
    
6. Greifen Sie auf den markierten Nachrichtentext über [IStream](http://msdn.microsoft.com/en-us/library/aa380034%28VS.85%29.aspx) -Methoden, und senden Sie sie an die messaging-System. 
    
 **Zum Abrufen von gekapselte Eigenschaften**
  
1. Schreiben von Eigenschaften in eine neue Nachricht, einschließlich Nachrichtentext für die markierte, die die gekapselten Eigenschaften enthält, die messaging-System unterstützt.
    
2. Decodiert den TNEF-Stream aus der entsprechenden Anlage.
    
3. Alle anderen Anlagen decodieren und in neue MAPI-Anlagen auf eine Nachricht zu schreiben.
    
4. Öffnen Sie den TNEF-Stream für die Decodierung mit der Funktion [OpenTnefStreamEx](opentnefstreamex.md) . 
    
5. Verwenden Sie die [ITnef::ExtractProps](itnef-extractprops.md) -Methode zum Decodieren des TNEF-Streams und die gekapselten Eigenschaften in die neue Nachricht zu schreiben. Codierten Eigenschaften, die Duplikate der nonencoded Eigenschaften sind überschreibt die nonencoded Eigenschaften, wenn die codierten Eigenschaften decodiert werden. 
    
6. Verwenden Sie die [ITnef::OpenTaggedBody](itnef-opentaggedbody.md) -Methode zum Analysieren des Nachrichtentext Anlage Positionen von Tags in den Nachrichtentext wiederhergestellt werden. 
    

