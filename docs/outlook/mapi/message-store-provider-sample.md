---
title: Beispiel für nachrichten Store Anbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c9cd4c62dfff127763494c2edab0a3ec47ee9413
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59571416"
---
# <a name="message-store-provider-sample"></a>Beispiel für nachrichten Store Anbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der PsT-Store-Anbieter verwendet einen PST-Anbieter (Personal Folders File) als Back-End zum Speichern von Daten. Der anbieterumschlossene PST-Speicher sollte zusammen mit der Replikations-API verwendet werden. 
  
Mit der Replikations-API können Sie Elemente aus einem Back-End-Daten-Repository in einen Microsoft Outlook PST-Speicher replizieren. Verwenden Sie die Replikations-API, um die Daten in einen dedizierten PST-Speicher zu replizieren und den Synchronisierungsstatus nachzuverfolgen. Weitere Informationen finden Sie unter ["Informationen zur Replikations-API".](about-the-replication-api.md)
  
Die meisten Funktionen im Sample Wrapped PST Store Provider übergeben ihre Argumente direkt an den zugrunde liegenden PST-Anbieter. Bestimmte Funktionen erfordern eine spezielle Implementierung und werden in den folgenden Themen beschrieben.
  
|||
|:-----|:-----|
|Ausführbaren:  <br/> |WrpPST32.dll  <br/> |
|Quellcodeverzeichnis:  <br/> |SampleWrappedPSTStoreProvider\WrapPST  <br/> |
|Sprache:  <br/> |C++  <br/> |
|Plattformen:  <br/> |Microsoft Visual Studio 2008 zum Kompilieren für Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Unterstützte Features

Dieses Beispiel unterstützt Microsoft Outlook 2010 64-Bit und wurde nun für Outlook 2013 überarbeitet. Weitere Informationen finden Sie in den folgenden Themen:
  
- [Informationen über die Replikations-API](about-the-replication-api.md)
    
- [Initialisieren eines Anbieters von umschlossenen PST-Store](initializing-a-wrapped-pst-store-provider.md)
    
- [Anmelden bei einem Anbieter von umschlossenen PST-Store](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [Verwenden eines Anbieters von umschlossenen PST-Store](using-a-wrapped-pst-store-provider.md)
    
- [Herunterfahren eines Anbieters von umschlossenen PST-Store](shutting-down-a-wrapped-pst-store-provider.md)
    
 **So installieren Sie den PsT-Beispielanbieter Store**
  
1. Informationen zum Herunterladen des Beispielanbieters für umschlossene PST finden Sie unter ["Herunterladen der Outlook MAPI-Beispiele".](downloading-the-outlook-mapi-samples.md)
    
2. Suchen Sie den Ordner, in dem Sie die Outlook MAPI-Beispiele gespeichert haben. Klicken Sie mit der rechten Maustaste auf den Ordner **"OutlookMAPISamples- \<version number\>** zip", und klicken Sie dann auf **"Alle extrahieren".**
    
3. Klicken Sie auf **Durchsuchen,** wählen Sie den Speicherort aus, an dem Sie das Beispiel speichern möchten, und klicken Sie dann auf **"Extrahieren".**
    
4. Führen Sie Microsoft Visual Studio 2008 aus.
    
5. Klicken Sie in Microsoft Visual Studio 2008 auf **"Datei",** wählen Sie **"Öffnen"** aus, und klicken Sie dann auf **Project/Lösung.**
    
6. Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie auf **"WrapPST.vcproj",** und klicken Sie dann auf **"Öffnen".**
    
7. On the **Build** menu, click **Build Solution**.
    
8. Klicken Sie im Dialogfeld **"Datei speichern unter"** auf **"Speichern".**
    
9. Klicken Sie in dem Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste auf die **Dateiinstall.bat,** und klicken Sie dann **auf "Als Administrator ausführen".**
    
10. Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.
    

