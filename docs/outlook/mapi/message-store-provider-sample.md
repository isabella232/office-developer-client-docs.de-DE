---
title: Beispiel für Nachrichtenspeicher Anbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: eb51881aac6e1953a21686857944ba2a15d0dca2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356938"
---
# <a name="message-store-provider-sample"></a>Beispiel für Nachrichtenspeicher Anbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Beispiel-Wrapped-PST-Speicheranbieter verwendet einen PST-Anbieter als Back-End zum Speichern von Daten. Der eingebundene PST-Speicheranbieter sollte zusammen mit der Replikations-API verwendet werden. 
  
Mit der Replikations-API können Sie Elemente aus einem Back-End-Daten-Repository in einen Microsoft Outlook-PST-Speicher replizieren. Sie verwenden die Replikations-API, um die Daten in einem dedizierten PST-Speicher zu replizieren und den Synchronisierungsstatus nachzuverfolgen. Weitere Informationen finden Sie unter [Informationen zur Replikations-API](about-the-replication-api.md).
  
Die meisten Funktionen im beispielhaften PST-Speicheranbieter übergeben ihre Argumente direkt an den zugrunde liegenden PST-Anbieter. Bestimmte Funktionen erfordern eine spezielle Implementierung und werden in den folgenden Themen beschrieben.
  
|||
|:-----|:-----|
|Executable  <br/> |WrpPST32. dll  <br/> |
|Quellcodeverzeichnis:  <br/> |SampleWrappedPSTStoreProvider\WrapPST  <br/> |
|Sprache  <br/> |C++  <br/> |
|Plattformen  <br/> |Microsoft Visual Studio 2008 für die Kompilierung für Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Unterstützte Features

In diesem Beispiel wird Microsoft Outlook 2010 64-Bit unterstützt und nun für Outlook 2013 überarbeitet. Weitere Informationen finden Sie in den folgenden Themen:
  
- [Informationen über die Replikations-API](about-the-replication-api.md)
    
- [Initialisieren eines einGebundenen PST-Speicheranbieters](initializing-a-wrapped-pst-store-provider.md)
    
- [Anmelden bei einem einGebundenen PST-Speicheranbieter](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [Verwenden eines einGebundenen PST-Speicheranbieters](using-a-wrapped-pst-store-provider.md)
    
- [Herunterfahren eines einGebundenen PST-Speicheranbieters](shutting-down-a-wrapped-pst-store-provider.md)
    
 **So installieren Sie den beispielhaften PST-Speicheranbieter**
  
1. Informationen zum Herunterladen des Beispiel-Wrapper-PST-Anbieters finden Sie unter [herunterladen der Outlook-MAPI-Beispiele](downloading-the-outlook-mapi-samples.md).
    
2. Suchen Sie den Ordner, in dem Sie die Outlook-MAPI-Beispiele gespeichert haben. Klicken Sie mit der rechten Maustaste auf den Zip **-Ordner OutlookMAPISamples-\<Versions\> Nummer** , und klicken Sie dann auf **Alle extrahieren**.
    
3. Klicken Sie auf **Durchsuchen**, wählen Sie den Speicherort aus, an dem Sie das Beispiel speichern möchten, und klicken Sie dann auf **extrahieren**.
    
4. Führen Sie Microsoft Visual Studio 2008 aus.
    
5. Klicken Sie in Microsoft Visual Studio 2008 auf **Datei**, wählen Sie **Öffnen**aus, und klicken Sie dann auf **Projekt/Lösung**.
    
6. Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie auf **WrapPST. vcproj**, und klicken Sie dann auf **Öffnen**.
    
7. On the **Build** menu, click **Build Solution**.
    
8. Klicken Sie im Dialogfeld **Datei speichern** unter auf **Speichern**.
    
9. Klicken Sie in dem Ordner, in dem Sie das Beispiel gespeichert haben, mit der rechten Maustaste auf die Datei **install. bat** , und klicken Sie dann auf **als Administrator ausführen**.
    
10. Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.
    

