---
title: Beispiel für Store-Anbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1e4077b-7a95-440d-a326-a8dc9cdab4fe
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: eb51881aac6e1953a21686857944ba2a15d0dca2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436867"
---
# <a name="message-store-provider-sample"></a>Beispiel für Store-Anbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Der Beispielanbieter für Store PST verwendet einen Anbieter für persönliche Ordner als Back-End zum Speichern von Daten. Der umschlossene ANBIETER für den PST-Speicher sollte zusammen mit der Replikations-API verwendet werden. 
  
Mit der Replikations-API können Sie Elemente aus einem Back-End-Datenrepository in einen Microsoft Outlook PST Store replizieren. Sie verwenden die Replikations-API, um die Daten in einen dedizierten PST-Speicher zu replizieren und den Synchronisierungsstatus zu verfolgen. Weitere Informationen finden Sie unter [Informationen zur Replikations-API](about-the-replication-api.md).
  
Die meisten Funktionen im Beispielanbieter für umschlossene STORE übergeben ihre Argumente direkt an den zugrunde liegenden PST-Anbieter. Bestimmte Funktionen erfordern eine spezielle Implementierung und werden in den folgenden Themen beschrieben.
  
|||
|:-----|:-----|
|Ausführbare Datei:  <br/> |WrpPST32.dll  <br/> |
|Quellcodeverzeichnis:  <br/> |SampleWrappedPSTStoreProvider\WrapPST  <br/> |
|Sprache:  <br/> |C++  <br/> |
|Plattformen:  <br/> |Microsoft Visual Studio 2008 zum Kompilieren für Windows Vista, Windows Server 2008, Windows XP SP2 und Windows Server 2003 SP1  <br/> |
   
## <a name="supported-features"></a>Unterstützte Features

Dieses Beispiel unterstützt Microsoft Outlook 2010 64-Bit und wurde nun für Outlook 2013 überarbeitet. Weitere Informationen finden Sie in den folgenden Themen:
  
- [Informationen über die Replikations-API](about-the-replication-api.md)
    
- [Initialisieren eines umschlossenen STORE Anbieters](initializing-a-wrapped-pst-store-provider.md)
    
- [Anmelden bei einem umschlossenen STORE Anbieter](logging-on-to-a-wrapped-pst-store-provider.md)
    
- [Verwenden eines umschlossenen STORE Anbieters](using-a-wrapped-pst-store-provider.md)
    
- [Herunterfahren eines umschlossenen STORE Anbieters](shutting-down-a-wrapped-pst-store-provider.md)
    
 **So installieren Sie den Beispielanbieter für Store PST**
  
1. Informationen zum Herunterladen des Beispielanbieters für umschlossene PST finden Sie unter [Herunterladen der Outlook MAPI-Beispiele](downloading-the-outlook-mapi-samples.md).
    
2. Suchen Sie den Ordner, in dem Sie die Outlook gespeichert haben. Klicken Sie mit der rechten Maustaste auf den **Ordner OutlookMAPISamples- \< version number \>** zip, und klicken Sie dann auf Alle **extrahieren.**
    
3. Klicken **Sie auf Durchsuchen,** wählen Sie den Speicherort aus, an dem Sie das Beispiel speichern möchten, und klicken Sie dann auf **Extrahieren**.
    
4. Führen Microsoft Visual Studio 2008 aus.
    
5. Klicken Microsoft Visual Studio 2008 auf **Datei,** wählen Sie **Öffnen** aus, und klicken Sie **dann auf Project/Lösung**.
    
6. Navigieren Sie zu dem Speicherort, an dem Sie das Beispiel gespeichert haben, klicken Sie auf **WrapPST.vcproj,** und klicken Sie dann auf **Öffnen**.
    
7. On the **Build** menu, click **Build Solution**.
    
8. Klicken Sie im Dialogfeld Datei speichern **unter** auf **Speichern**.
    
9. Klicken Sie im Ordner, in dem Sie das Beispiel gespeichert **haben,** mit der rechten Maustaste aufinstall.batdatei, und klicken Sie dann **auf Als Administrator ausführen**.
    
10. Klicken Sie im Dialogfeld **Benutzerkontensteuerung** auf **Weiter**.
    

