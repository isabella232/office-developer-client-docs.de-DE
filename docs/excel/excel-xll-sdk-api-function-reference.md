---
title: Excel XLL SDK – API-Funktionsreferenz
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- API-Funktionsreferenz [Excel 2007],Funktionen [Excel 2007],Referenz [Excel 2007],Excel 2007 XLL Software Development Kit, Referenz
api_type:
- COM
ms.assetid: 2f6df879-7546-4ac0-a4e3-6b009aee9463
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.localizationpriority: high
ms.openlocfilehash: 998d279258294657624d2ee9673947bd96bf8569
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621451"
---
# <a name="excel-xll-sdk-api-function-reference"></a>Excel XLL SDK – API-Funktionsreferenz

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Das Microsoft Excel 2013 XLL SDK enthält die Quelldateien für eine "Framework"-Bibliothek, die das Schreiben von XLLs beschleunigen soll, sowie die zwei Beispielprojekte "Example" und "Generic". 
  
Dieser Abschnitt stellt eine Funktionsreferenz für Folgendes bereit:
  
- Excel-Rückrufe, die die XLL aufrufen kann
    
- XLL-Rückrufe, nach denen Microsoft Excel sucht
    
- Wichtige Funktionen in den Beispiel- und Frameworkprojekten.
    
## <a name="sample-projects"></a>Beispielprojekte

Das Excel 2013 XLL SDK enthält Quelldateien und Microsoft Visual Studio Project-Dateien für die folgenden Beispielprojekte:
  
- Das **Framework**-Projekt (`SAMPLES\FRAMEWRK\`) enthält ein Projekt, aus dem die Bibliothek FRAMEWRK.lib erstellt werden kann, die anschließlich mit anderen XLL-Projekten verknüpft werden kann. Die Bibliothek enthält viele Funktionen und Tools, die das Schreiben von XLLs vereinfachen. Diese Bibliothek wird in den beiden anderen Projekten in Verbindung mit der Headerdatei FRAMEWRK.h verwendet.
    
- Das Projekt **Example** enthält ein Projekt (`SAMPLES\EXAMPLE\`), aus dem die XLL-Datei EXAMPLE.xll, erstellt werden kann. Die XLL enthält viele Beispiele für die Verwendung der Bibliothek "Framework" sowie Beispielimplementierungen der XLL-Add-in-Schnittstellenfunktionen wie z. B. **xlAutoOpen**.
    
- Das Projekt **Generic** (`SAMPLES\GENERIC\`) enthält ein Projekt, aus dem die XLL-Datei GENERIC.xll erstellt werden kann. Die XLL veranschaulicht verschiedene Beispielfunktionen und -befehle und ist ein guter Ausgangspunkt für das Schreiben eigener XLLs.
    
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Add-In-Manager und XLL-Benutzeroberflächenfunktionen](add-in-manager-and-xll-interface-functions.md)
  
- [C-API-Rückruffunktionen Excel4, Excel12](c-api-callback-functions-excel4-excel12.md)
  
- [Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)
  
- [C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
- [Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)
  
- [Funktionen in der generische DLL](functions-in-the-generic-dll.md)
  
- [Excel-Clusterconnector-Funktionen](excel-cluster-connector-functions.md)
  
## <a name="see-also"></a>Siehe auch

- [Programmieren mit der C-API in Excel](programming-with-the-c-api-in-excel.md)
  
- [Entwickeln von XLLs für Excel](developing-excel-xlls.md)

