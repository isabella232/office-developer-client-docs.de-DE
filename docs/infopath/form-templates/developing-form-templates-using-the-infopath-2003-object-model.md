---
title: Entwickeln von Formularvorlagen mithilfe des InfoPath-Objektmodells 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Formularvorlagen [InfoPath 2007] mit InfoPath 2003-Objektmodell, InfoPath 2003-kompatible Formularvorlagen, InfoPath 2007, entwickeln von Formularvorlagen mit InfoPath 2003-Objektmodell, Objektmodelle [InfoPath 2003], entwickeln von Formularvorlagen mit verwaltetem Code
localization_priority: Normal
ms.assetid: c74cbcd0-4fe6-4eb7-a05c-f61e1868c42b
description: Microsoft InfoPath unterstützt weiterhin Formularvorlagenprojekte, die mit Microsoft Office InfoPath 2003 Toolkit für Visual Studio .NET oder Visual Studio 2005-Tools für Microsoft Office System erstellt wurden und die Geschäftslogik für die Mitglieder der Microsoft. Office. Interop. InfoPath. SemiTrust-Namespace. In den Themen in diesem Abschnitt werden die Typen und Member dieses Namespace als InfoPath 2003-kompatibles Objektmodell oder einfach als InfoPath 2003-Objektmodell bezeichnet. InfoPath unterstützt auch mit Microsoft Office InfoPath 2007 erstellte Formularvorlagenprojekte, die das InfoPath 2003-kompatible Objektmodell verwenden. Darüber hinaus können Sie mithilfe von InfoPath neue Formularvorlagenprojekte erstellen, die InfoPath 2003-kompatibles Objektmodell verwenden, um die Abwärtskompatibilität für Benutzer von Office InfoPath 2007 beizubehalten. Alle Themen in diesem Abschnitt sind spezifisch für das Erstellen und entwickeln von Formularvorlagen, die mit dem InfoPath 2003-kompatiblen Objektmodell arbeiten, das vom Microsoft. Office. Interop. InfoPath. SemiTrust-Namespace bereitgestellt wird.
ms.openlocfilehash: a39f921f6c7465dbcf469062b866c808fa222851
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300364"
---
# <a name="developing-form-templates-using-the-infopath-2003-object-model"></a>Entwickeln von Formularvorlagen mithilfe des InfoPath-Objektmodells 2003

Microsoft InfoPath unterstützt weiterhin Formularvorlagenprojekte, die mit Microsoft Office InfoPath 2003 Toolkit für Visual Studio .NET oder Visual Studio 2005-Tools für Microsoft Office System erstellt wurden und die Geschäftslogik für die Mitglieder [der Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace. In den Themen in diesem Abschnitt werden die Typen und Member dieses Namespace als InfoPath 2003-kompatibles Objektmodell oder einfach als InfoPath 2003-Objektmodell bezeichnet. InfoPath unterstützt auch mit Microsoft Office InfoPath 2007 erstellte Formularvorlagenprojekte, die das InfoPath 2003-kompatible Objektmodell verwenden. Darüber hinaus können Sie mithilfe von InfoPath neue Formularvorlagenprojekte erstellen, die InfoPath 2003-kompatibles Objektmodell verwenden, um die Abwärtskompatibilität für Benutzer von Office InfoPath 2007 beizubehalten. Alle Themen in diesem Abschnitt sind spezifisch für das Erstellen und entwickeln von Formularvorlagen, die mit dem InfoPath 2003-kompatiblen Objektmodell arbeiten, das vom [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace bereitgestellt wird. 
  
> [!IMPORTANT]
> Obwohl das Erstellen von Geschäftslogik mit dem vom [Microsoft. Office. Interop. InfoPath. SemiTrust](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.aspx) -Namespace bereitgestellten Objektmodell mit verwaltetem Code von InfoPath weiterhin unterstützt wird, wird die mit diesem Objektmodell geschriebene Geschäftslogik nicht unterstützt. browserfähige Formularvorlagen, die für Microsoft SharePoint Server 2010 mit InfoPath Forms Services bereitgestellt werden. Browser fähige Formularvorlagen müssen das neue InfoPath-Objektmodell mit verwaltetem Code verwenden, das von Mitgliedern des [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespaces für benutzerdefinierte Geschäftslogik bereitgestellt wird. Weitere Informationen zum Erstellen von Formularvorlagen mit Geschäftslogik, die mit Mitgliedern des [Microsoft. Office. InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) -Namespaces geschrieben wurde, finden Sie unter [entwickeln von InfoPath-Formularvorlagen mit Code](developing-infopath-form-templates-with-code.md). > beachten Sie außerdem, dass Benutzer von Formularvorlagen, die mit Visual Studio 2012 kompiliert wurden, Microsoft .NET Framework 2,0 oder höher auf ihren Computern installiert haben müssen. Bei Benutzern von Formularvorlagen, die mit Visual Studio .NET 2003 kompiliert wurden, muss nur Microsoft .NET Framework 1.1 auf dem Computer installiert sein. 
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

[Erste Schritte beim Entwickeln von Formularvorlagen mit dem InfoPath-Objektmodell 2003](get-started-developing-form-templates-using-infopath-object-model.md)
  
> Enthält Informationen zum erstmaligen Erstellen von Formularvorlagen mit verwaltetem Code, in denen das InfoPath 2003-kompatible Objektmodell verwendet wird.
    
[Erstellen von Formularvorlagen mit dem InfoPath-Objektmodell 2003](creating-form-templates-using-the-infopath-2003-object-model.md)
  
> Erläutert Themen wie Initialisierungs- und Bereinigungscode, das Hinzufügen von Ereignishandlern, das Debuggen und Bereitstellen von Formularvorlagen mit verwaltetem Code, die Threadunterstützung und das Arbeiten mit Microsoft XML Core Services (MSXML) aus InfoPath-Lösungen mit verwaltetem Code heraus.
    
[Sicherheit in InfoPath-Formularvorlagen mit Code](security-in-infopath-form-templates-with-code.md)
  
> Erläutert das Sicherheitsmodell für InfoPath-Formularvorlagen mit verwaltetem Code, das Debuggen voll vertrauenswürdiger InfoPath-Formularvorlagen und verwandte Sicherheitsverfahren.
    
[Grundlegendes zum InfoPath 2003-Objektmodell](understanding-the-infopath-2003-object-model.md)
  
> Erläutert das InfoPath 2003-kompatible Objektmodell und allgemeine Programmieraufgaben für Formularvorlagen mit verwaltetem Code, in denen dieses Objektmodell verwendet wird.
    
[Problembehandlung bei Formularvorlagen, die das InfoPath 2003-Objektmodell verwenden](troubleshoot-form-templates-that-use-infopath-object-model.md)
  
> Enthält Tipps zum Beheben häufig vorkommender Probleme, die beim Erstellen von Formularvorlagen mit verwaltetem Code auftreten können, in denen das InfoPath 2003-kompatible Objektmodell verwendet wird.
    
## <a name="related-sections"></a>Verwandte Abschnitte

[InfoPath-Entwickler Portal](https://go.microsoft.com/fwlink?LinkID=11689)
  
> Enthält Links zu technischen Artikeln, Codebeispielen, Downloads, Support sowie sonstige MSDN-Dokumentationen zum Erstellen benutzerdefinierter InfoPath-Lösungen.
    
[Office Developer Center](https://go.microsoft.com/fwlink?LinkID=27128)
  
> Enthält Links zu technischen Artikeln, Codebeispielen, Downloads, Support sowie sonstige MSDN-Dokumentationen zum Erstellen benutzerdefinierter Office-Lösungen.
    

