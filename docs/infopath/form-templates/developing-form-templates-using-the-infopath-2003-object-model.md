---
title: Entwickeln von Formularvorlagen mithilfe des InfoPath 2003-Objektmodells
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Formularvorlagen [infopath 2007], using infopath 2003 object model,InfoPath 2003-compatible form templates,InfoPath 2007, developing form templates using InfoPath 2003 object model,object models [InfoPath 2003], developing managed code form templates
ms.localizationpriority: medium
ms.assetid: c74cbcd0-4fe6-4eb7-a05c-f61e1868c42b
description: Microsoft InfoPath unterstützt weiterhin Formularvorlagenprojekte, die mit Microsoft Office InfoPath 2003 Toolkit für Visual Studio .NET oder Visual Studio 2005 Tools for the Microsoft Office System erstellt wurden, für die Geschäftslogik für Mitglieder von Microsoft geschrieben wurde. Office.Interop.InfoPath.SemiTrust-Namespace. In den Themen in diesem Abschnitt werden die Typen und Member dieses Namespace als InfoPath 2003-kompatibles Objektmodell oder einfach als InfoPath 2003-Objektmodell bezeichnet. InfoPath unterstützt auch Formularvorlagenprojekte, die mit Microsoft Office InfoPath 2007 erstellt wurden und das InfoPath 2003-kompatible Objektmodell verwenden. Darüber hinaus können Sie InfoPath verwenden, um neue Formularvorlagenprojekte zu erstellen, die das InfoPath 2003-kompatible Objektmodell verwenden, um die Abwärtskompatibilität für Benutzer von Office InfoPath 2007 beizubehalten. Alle Themen in diesem Abschnitt beziehen sich speziell auf das Erstellen und Entwickeln von Formularvorlagen, die mit dem von Microsoft bereitgestellten InfoPath 2003-kompatiblen Objektmodell arbeiten. Office.Interop.InfoPath.SemiTrust-Namespace.
ms.openlocfilehash: 8f481f49e56a45dfaf6d84298f80485a733a7665
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621276"
---
# <a name="developing-form-templates-using-the-infopath-2003-object-model"></a>Entwickeln von Formularvorlagen mithilfe des InfoPath 2003-Objektmodells

Microsoft InfoPath unterstützt weiterhin Formularvorlagenprojekte, die mit Microsoft Office InfoPath 2003 Toolkit für Visual Studio .NET oder Visual Studio 2005 Tools for the Microsoft Office System erstellt wurden, für die Geschäftslogik für Mitglieder des [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) geschrieben wurde. In den Themen in diesem Abschnitt werden die Typen und Member dieses Namespace als InfoPath 2003-kompatibles Objektmodell oder einfach als InfoPath 2003-Objektmodell bezeichnet. InfoPath unterstützt auch Formularvorlagenprojekte, die mit Microsoft Office InfoPath 2007 erstellt wurden und das InfoPath 2003-kompatible Objektmodell verwenden. Darüber hinaus können Sie InfoPath verwenden, um neue Formularvorlagenprojekte zu erstellen, die das InfoPath 2003-kompatible Objektmodell verwenden, um die Abwärtskompatibilität für Benutzer von Office InfoPath 2007 beizubehalten. Alle Themen in diesem Abschnitt beziehen sich speziell auf das Erstellen und Entwickeln von Formularvorlagen, die mit dem InfoPath 2003-kompatiblen Objektmodell arbeiten, das vom [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) bereitgestellt wird. 
  
> [!IMPORTANT]
> Obwohl das Erstellen von Geschäftslogik mit dem objektmodell mit verwaltetem Code, das vom [Microsoft.Office.Interop.InfoPath.SemiTrust-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) bereitgestellt wird, weiterhin von InfoPath unterstützt wird, wird die mit diesem Objektmodell geschriebene Geschäftslogik für browserfähige Formularvorlagen, die für Microsoft SharePoint Server 2010 mit InfoPath Forms Services bereitgestellt werden, nicht unterstützt. Browserfähige Formularvorlagen müssen das neue InfoPath-Objektmodell mit verwaltetem Code verwenden, das von Mitgliedern der [Microsoft.Office bereitgestellt wird. InfoPath-Namespace](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) für benutzerdefinierte Geschäftslogik. Weitere Informationen zum Erstellen von Formularvorlagen mit Geschäftslogik, die mit Mitgliedern der [Microsoft.Office geschrieben wurde. InfoPath-Namespace:](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) [Entwickeln von InfoPath-Formularvorlagen mit Code.](developing-infopath-form-templates-with-code.md) > Beachten Sie außerdem, dass Für Benutzer von Formularvorlagen, die mit Visual Studio 2012 kompiliert wurden, Microsoft .NET Framework 2.0 oder höher auf ihren Computern installiert sein muss. Bei Benutzern von Formularvorlagen, die mit Visual Studio .NET 2003 kompiliert wurden, muss nur Microsoft .NET Framework 1.1 auf dem Computer installiert sein. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[Erste Schritte beim Entwickeln von Formularvorlagen mithilfe des InfoPath 2003-Objektmodells](get-started-developing-form-templates-using-infopath-object-model.md)
  
> Enthält Informationen zum erstmaligen Erstellen von Formularvorlagen mit verwaltetem Code, in denen das InfoPath 2003-kompatible Objektmodell verwendet wird.
    
[Erstellen von Formularvorlagen mithilfe des InfoPath 2003-Objektmodells](creating-form-templates-using-the-infopath-2003-object-model.md)
  
> Erläutert Themen wie Initialisierungs- und Bereinigungscode, das Hinzufügen von Ereignishandlern, das Debuggen und Bereitstellen von Formularvorlagen mit verwaltetem Code, die Threadunterstützung und das Arbeiten mit Microsoft XML Core Services (MSXML) aus InfoPath-Lösungen mit verwaltetem Code heraus.
    
[Sicherheit in InfoPath-Formularvorlagen mit Code](security-in-infopath-form-templates-with-code.md)
  
> Erläutert das Sicherheitsmodell für InfoPath-Formularvorlagen mit verwaltetem Code, das Debuggen voll vertrauenswürdiger InfoPath-Formularvorlagen und verwandte Sicherheitsverfahren.
    
[Grundlegendes zum InfoPath 2003-Objektmodell](understanding-the-infopath-2003-object-model.md)
  
> Erläutert das InfoPath 2003-kompatible Objektmodell und allgemeine Programmieraufgaben für Formularvorlagen mit verwaltetem Code, in denen dieses Objektmodell verwendet wird.
    
[Problembehandlung bei Formularvorlagen, die das InfoPath 2003-Objektmodell verwenden](troubleshoot-form-templates-that-use-infopath-object-model.md)
  
> Enthält Tipps zum Beheben häufig vorkommender Probleme, die beim Erstellen von Formularvorlagen mit verwaltetem Code auftreten können, in denen das InfoPath 2003-kompatible Objektmodell verwendet wird.
    
## <a name="related-sections"></a>Verwandte Abschnitte

[InfoPath-Entwicklerportal](https://go.microsoft.com/fwlink?LinkID=11689)
  
> Enthält Links zu technischen Artikeln, Codebeispielen, Downloads, Support sowie sonstige MSDN-Dokumentationen zum Erstellen benutzerdefinierter InfoPath-Lösungen.
    
[Office Developer Center](https://go.microsoft.com/fwlink?LinkID=27128)
  
> Enthält Links zu technischen Artikeln, Codebeispielen, Downloads, Support sowie sonstige MSDN-Dokumentationen zum Erstellen benutzerdefinierter Office-Lösungen.
    

