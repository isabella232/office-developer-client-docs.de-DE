---
title: Informationen zur InfoPath-XML-Interopassembly
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- msxml interop [infopath 2007],InfoPath 2007, PRIMÄRE XML-Interopassembly,InfoPath XML-Interopassembly
ms.localizationpriority: medium
ms.assetid: fb28659b-8a71-4f43-9121-2c748fb2c5e1
description: Die InfoPath-XML-Interopassembly wird bereitgestellt, um unterstützung für die Interoperabilität zwischen verwaltetem Code und dem COM-Server zu ermöglichen, der von Microsoft XML Core Services (MSXML) aus externen Anwendungen verfügbar gemacht wird, die InfoPath automatisieren.
ms.openlocfilehash: bae183892569652a41e62b302518fb43b933a370
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572347"
---
# <a name="about-the-infopath-xml-interop-assembly"></a>Informationen zur InfoPath-XML-Interopassembly

Die InfoPath-XML-Interopassembly wird bereitgestellt, um unterstützung für die Interoperabilität zwischen verwaltetem Code und dem COM-Server zu ermöglichen, der von Microsoft XML Core Services (MSXML) aus externen Anwendungen verfügbar gemacht wird, die InfoPath automatisieren.

Die **Option .NET Programmability Support** im InfoPath-Setupprogramm installiert drei Interopassemblys. Interop-Assemblys sind .NET-Assemblys, die als Verbindung zwischen verwaltetem und nicht verwaltetem Code dienen, indem sie COM-Objektmember entsprechenden verwalteten .NET-Membern zuordnen. Eine dieser Assemblys, Microsoft.Office.Interop.InfoPath.Xml.dll, stellt die Member des [Microsoft.Office.Interop.InfoPath.Xml-Namespace](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.infopath.xml?view=infopath-external) bereit, der verwendet wird, um mit Membern zu arbeiten, die vom COM-Server für Microsoft XML Core Services (MSXML) aus externen Anwendungen verfügbar gemacht werden, die InfoPath mit verwaltetem Code automatisieren. 
  
> [!NOTE]
> Die Verweise auf die Microsoft.Office.Interop.InfoPath.dll und Microsoft.Office.Interop.InfoPath.Xml.dll Interopassemblys, die für externe InfoPath-Automatisierungsprojekte erforderlich sind, müssen manuell eingerichtet werden. Weitere Informationen zur externen Automatisierung finden Sie unter ["Szenarien und Beispiele für externe Automatisierung".](external-automation-scenarios-and-examples.md) 
  
## <a name="see-also"></a>Siehe auch

- [Arbeiten mit MSXML und System.Xml mit dem InfoPath 2003-Objektmodell](https://msdn.microsoft.com/library/f7a0cac5-26f9-49ed-b52c-0240ef0c9d38%28Office.15%29.aspx)

