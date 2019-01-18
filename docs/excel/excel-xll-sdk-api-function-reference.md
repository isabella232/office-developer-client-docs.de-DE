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
localization_priority: Priority
ms.openlocfilehash: e116021a3dc24de7decbe0dad76cc762cd66d032
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715956"
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
  
- Das Projekt **Framework** (`SAMPLES\FRAMEWRK\`) enthält ein Projekt, aus dem die Bibliothek FRAMEWRK.lib erstellt werden kann, die dann mit anderen XLL-Projekten verknüpft werden kann. Die Bibliothek enthält viele Funktionen und Tools, die das Schreiben von XLLs einfacher machen. Diese Bibliothek wird in den beiden anderen Projekten zusammen mit der Headerdatei FRAMEWRK.h verwendet.
    
- Das Projekt **Example** (`SAMPLES\EXAMPLE\`) enthält ein Projekt, aus dem die XLL-Datei EXAMPLE.xll erstellt werden kann. Die XLL enthält viele Beispiele für die Verwendung der Bibliothek „Framework“ sowie Beispielimplementierungen der XLL-Add-In-Schnittstellenfunktionen wie z. B. **xlAutoOpen**.
    
- Das Projekt **Generic** (`SAMPLES\GENERIC\`) enthält ein Projekt, aus dem die XLL-Datei GENERIC.xll erstellt werden kann. Die XLL veranschaulicht verschiedene Beispiele für Funktionen und Befehle und ist ein guter Ausgangspunkt zum Schreiben Ihrer eigenen XLLs.
    
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

