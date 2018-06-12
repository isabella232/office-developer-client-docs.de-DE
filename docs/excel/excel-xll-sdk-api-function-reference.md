---
title: Excel XLL-SDK-API-Funktionsreferenz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- api function reference [excel 2007],functions [Excel 2007],reference [Excel 2007],Excel 2007 XLL Software Development Kit, reference
localization_priority: Normal
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2bb0a57ebcae618c8e921135b2bd4c50e8adf751
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790497"
---
# <a name="excel-xll-sdk-api-function-reference"></a>Excel XLL-SDK-API-Funktionsreferenz

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Das Microsoft Excel 2013 XLL SDK enth�lt die Quelldateien f�r eine "Framework"-Bibliothek, die das Schreiben von XLLs beschleunigen soll, sowie die zwei Beispielprojekte "Example" und "Generic". 
  
Dieser Abschnitt stellt eine Funktionsreferenz f�r Folgendes bereit:
  
- Excel-R�ckrufe, die die XLL aufrufen kann
    
- XLL-R�ckrufe, nach denen Microsoft Excel sucht
    
- Wichtige Funktionen in den Beispiel- und Frameworkprojekten
    
## <a name="sample-projects"></a>Beispiel-Projekte

Das Excel 2013 XLL SDK stellt Quelldateien und Microsoft Visual Studio-Projektdateien f�r die folgenden Beispielprojekte bereit:
  
- Das Projekt **Framework** (`SAMPLES\FRAMEWRK\`) enthält ein Projekt, das in einer Dokumentbibliothek, FRAMEWRK.lib, erstellt werden kann, die dann in andere Projekte XLL verknüpft werden können. Die Bibliothek enth�lt viele Funktionen und Tools, die das Schreiben von XLLs vereinfachen. Diese Bibliothek wird in den beiden anderen Projekten in Verbindung mit der Headerdatei FRAMEWRK.h verwendet.
    
- **Das Beispielprojekt** (`SAMPLES\EXAMPLE\`) enthält ein Projekt, das auf eine XLL, EXAMPLE.xll erstellt werden kann. Die XLL enthält viele Beispiele in diesem Beispiel wird die Implementierung der XLL-add-in-Schnittstelle-Funktionen wie **XlAutoOpen**und die Verwendung von der Framework-Klassenbibliothek.
    
- Das Projekt **generische** (`SAMPLES\GENERIC\`) enthält ein Projekt, das auf eine XLL, GENERIC.xll erstellt werden kann. Die XLL veranschaulicht verschiedene Beispielfunktionen und -befehle und ist ein guter Ausgangspunkt f�r das Schreiben eigener XLLs.
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Add-In-Manager und Funktionen von XLL-Schnittstelle](add-in-manager-and-xll-interface-functions.md)
  
- [C-API-R�ckruf funktioniert Excel4 Excel12](c-api-callback-functions-excel4-excel12.md)
  
- [Wichtige und n�tzliche C-API XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)
  
- [C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)
  
- [Funktionen in der generische DLL](functions-in-the-generic-dll.md)
  
- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a>Siehe auch

- [Programmieren mit der C-API in Excel](programming-with-the-c-api-in-excel.md)
  
- [Entwickeln von Excel-XLLs](developing-excel-xlls.md)

