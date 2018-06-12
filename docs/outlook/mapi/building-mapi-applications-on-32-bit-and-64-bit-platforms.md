---
title: Erstellen von MAPI-Anwendungen auf 32-Bit- und 64-Bit-Plattformen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d218ba2d-7a2e-4c33-a09b-a8c7e27f9726
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: dce3f4b5bfdcb34148c25c880d8d2d8173755b37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791377"
---
# <a name="building-mapi-applications-on-32-bit-and-64-bit-platforms"></a>Erstellen von MAPI-Anwendungen auf 32-Bit- und 64-Bit-Plattformen

**Betrifft**: Outlook 
  
In diesem Thema werden die Aktionen beschrieben, die MAPI-Entwickler zum �ndern und Neuerstellen von 32-Bit-MAPI-Anwendungen f�r die Ausf�hrung auf 64-Bit-Plattformen und von 64-Bit-Anwendungen f�r die Ausf�hrung auf 32-Bit-Plattformen durchf�hren m�ssen. In diesem Thema stellt die 64-Bit-Plattform ein Computer mit der 64-Bit-Version von Microsoft Outlook und Windows dar, und die 32-Bit-Plattform ein Computer mit der 32-Bit-Version von Outlook und der 32-Bit- oder 64-Bit-Version von Windows dar. 
  
## <a name="operating-system-and-office-support-for-64-bit-outlook"></a>Betriebssystem und Office-Unterstützung für 64-Bit-Outlook

> [!NOTE]
> [!HINWEIS] Der Begriff Bitanzahl bezieht sich auf die Unterscheidung zwischen 32-Bit- und 64-Bit-Prozessorarchitekturen und der zugeh�rigen Kompatibilit�t von Anwendungen. In diesem Thema wird Bitanzahl zum Angeben der Version von Windows, Microsoft Office, Outlook, oder einer MAPI-Anwendung, die entsprechend den Anforderungen einer 32-Bit- oder 64-Bit Prozessorarchitektur eines Computers und m�glicherweise anderer Programme, die auf diesem Computer ausgef�hrt werden, entwickelt wurde. 
  
Beginnend mit Microsoft Office 2010 steht Outlook als 32-Bit- und 64-Bit-Anwendung zur Verf�gung. Die Bitanzahl von Outlook auf einem bestimmten Computer h�ngt von der Bitanzahl des Windows-Betriebssystems (x86 oder x64) sowie, falls Office auf dem Computer installiert ist, von der Bitanzahl von Microsoft Office ab. Nachstehend finden Sie einige der Faktoren, von denen es abh�ngt, ob Sie eine 32-Bit- oder 64-Bit-Version von Outlook installieren k�nnen:
  
- 32-Bit-Versionen von Office (und 32-Bit-Versionen von Outlook) k�nnen unter einer 32-Bit- oder 64-Bit-Version des Windows-Betriebssystems installiert werden. 64-Bit-Versionen von Office (und 64-Bit-Versionen von Outlook) k�nnen nur unter einem 64-Bit-Betriebssystem installiert werden.
    
- Die Standardinstallation von Office unter einer 64-Bit-Version des Windows-Betriebssystems ist eine 32-Bit-Version von Office.
    
- Die Bitanzahl einer installierten Version von Outlook entspricht immer der Bitanzahl von Office, wenn Office auf dem gleichen Computer installiert ist. Mit anderen Worten, eine 32-Bit-Version von Outlook kann nicht auf einem Computer installiert werden, auf dem bereits 64-Bit-Versionen anderer Office-Anwendungen (beispielsweise eine 64-Bit-Version von Microsoft Word oder von Microsoft�Excel) installiert sind. Analog kann eine 64-Bit-Version von Outlook nicht auf einem Computer installiert werden, auf dem bereits 32-Bit-Versionen anderer Office-Anwendungen installiert sind.
    
## <a name="preparing-mapi-applications-for-32-bit-and-64-bit-platforms"></a>Vorbereiten der MAPI-Anwendungen für 32-Bit- und 64-Bit-Plattformen

Zu den MAPI-Anwendungen geh�ren eigenst�ndige Anwendungen wie beispielsweise Microsoft�Communicator und MFCMAPI sowie Dienstanbieter wie beispielsweise Adressbuch-, Speicher- und Transportanbieter. Für MAPI-Methode und die Funktion müssen Anrufe in einer MAPI-Anwendung (mit Ausnahme von Simple MAPI-Funktion MAPISendMail), funktioniert die Bitness der MAPI-Anwendung identisch mit der Bitness der MAPI-Subsystems auf dem Computer sein, denen die Anwendung zum gerichtet ist Führen Sie auf. Die Bitanzahl des MAPI-Subsystems wiederum wird durch die Bitanzahl der installierten Version von Outlook bestimmt und muss dieser immer entsprechen. In der folgenden Tabelle werden die erforderlichen Aktionen zur Vorbereitung von MAPI-Anwendungen f�r die Ausf�hrung auf Zielcomputern mit Office- und Windows-Versionen mit unterschiedlicher Bitanzahl aufgef�hrt.
  
|Bitanzahl der MAPI-Anwendung|Bitanzahl der Outlook-Version auf dem Zielcomputer|Bitanzahl der Windows-Version auf dem Zielcomputer|Erforderlichen Aktion, damit die Anwendung auf dem Zielcomputer ausgeführt werden kann|
|:-----|:-----|:-----|:-----|
|32-Bit  <br/> |32-Bit  <br/> |32-Bit- oder 64-bit  <br/> |Es sind keine weiteren Aktionen erforderlich.  <br/> |
|32-Bit  <br/> |64-Bit  <br/> |64-Bit  <br/> |Erstellen Sie die Anwendung als 64-Bit-Anwendung neu. Andernfalls tritt beim Ausf�hren aller MAPI-Methoden und -Funktionsaufrufen (mit Ausnahme von **MAPISendMail**) ein Fehler auf.  <br/> |
|64-Bit  <br/> |64-Bit  <br/> |64-Bit  <br/> |Es sind keine weiteren Aktionen erforderlich.  <br/> |
|64-Bit  <br/> |32-Bit  <br/> |32-Bit- oder 64-bit  <br/> |Erstellen Sie die Anwendung als 32-Bit-Anwendung neu. Andernfalls tritt beim Ausf�hren aller MAPI-Methoden und -Funktionsaufrufen (mit Ausnahme von **MAPISendMail**) ein Fehler auf.  <br/> |
   
In den folgenden Abschnitten werden die einzelnen Szenarien genauer erl�utert. Szenarien, die erfordern, Neuerstellen der MAPI-Anwendung, finden Sie unter [Link zu MAPI-Funktionen](how-to-link-to-mapi-functions.md) für Weitere Informationen zum Verknüpfen mit und MAPI-Funktionen aufrufen. 
  
### <a name="32-bit-mapi-application-and-32-bit-outlook"></a>MAPI-Anwendung 32-Bit- und 32-Bit-Outlook

MAPI-Anwendungen, die f�r ein 32-Bit-MAPI-Subsystem kompiliert wurden, das in 32-Bit-Versionen von Outlook, einschlie�lich der Versionen vor Microsoft Outlook 2013 verf�gbar ist, werden weiterhin auf Computern mit der 32-Bit-Version von Outlook und einer 32-Bit- oder 64-Bit-Version von Windows unterst�tzt. Anwendungsentwickler m�ssen keine weiteren Aktionen durchf�hren.
  
### <a name="32-bit-mapi-application-and-64-bit-outlook"></a>MAPI-Anwendung 32-Bit- und 64-Bit-Outlook

32-Bit-MAPI-Anwendungen werden nicht auf einem Computer mit der 64-Bit-Version von Outlook und der 64-Bit-Version von Windows unterst�tzt. Anwendungsentwickler m�ssen die Anwendung als 64-Bit-Anwendung f�r die 64-Bit-Plattform neu erstellen. Grund daf�r ist, dass eine 32-Bit-Anwendung die 64-Bit-Datei �Msmapi32.dll" nicht laden kann Es gibt eine kleine Anzahl von API-�nderungen, die Anwendungsentwickler vornehmen m�ssen, damit Ihr Code erfolgreich in einer 64-Bit-Umgebung ausgef�hrt werden kann. Diese �nderungen wurden an den MAPI-Headerdateien vorgenommen, damit 64-Bit-Plattformen unterst�tzt werden. Sie k�nnen diese Headerdateien unter [Outlook 2010: MAPI-Headerdateien](http://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1) herunterladen. Entwickler k�nnen denselben Satz von MAPI-Headerdateien zum Erstellen von 32-Bit- und 64-Bit-MAPI-Anwendungen verwenden.
  
### <a name="64-bit-mapi-application-and-64-bit-outlook"></a>MAPI-Anwendung 64-Bit- und 64-Bit-Outlook

64-Bit-MAPI-Anwendungen werden auf Computern mit der 64-Bit-Version von Outlook und der 64-Bit-Version von Windows unterst�tzt. Anwendungsentwickler m�ssen keine weiteren Aktionen durchf�hren.
  
### <a name="64-bit-mapi-application-and-32-bit-outlook"></a>MAPI-Anwendung 64-Bit- und 32-Bit-Outlook

64-Bit-MAPI-Anwendungen werden nicht auf einem Computer mit der 32-Bit-Version von Outlook und der 32-Bit- oder 64-Bit-Version von Windows unterst�tzt. Anwendungsentwickler m�ssen die Anwendung als 32-Bit-Anwendung f�r die Verwendung mit der 32-Bit-Version von Outlook neu erstellen. Verwenden Sie die aktualisierten MAPI-Headerdateien, die unter [Outlook 2010: MAPI-Headerdateien](http://www.microsoft.com/downloads/details.aspx?FamilyID=f8d01fc8-f7b5-4228-baa3-817488a66db1) heruntergeladen werden k�nnen. Entwickler k�nnen denselben Satz von MAPI-Headerdateien zum Erstellen von 32-Bit- und 64-Bit-MAPI-Anwendungen verwenden.
  
### <a name="exception-mapisendmail"></a>Ausnahme: MAPISendMail

Eine 32-Bit-MAPI-Anwendung darf in der Regel nicht auf einer 64-Bit-Plattform (64-Bit-Version von Outlook unter 64-Bit-Version von Windows) ausgef�hrt werden, ohne dass sie zun�chst als 64-Bit-Anwendung neu erstellt wird, und eine 64-Bit-MAPI-Anwendung darf nicht auf einem Computer mit der 32-Bit-Version von Outlook und der 32-Bit- oder 64-Bit-Version von Windows ausgef�hrt werden, ohne dass sie zun�chst als 32-Bit-Anwendung neu erstellt wird. In Abbildung�1 wird eine Warnmeldung dargestellt, die angezeigt wird. wenn eines dieser Szenarien auftritt.
  
**Abbildung 1. Fehlermeldung f�r die meisten bitanzahl�bergreifenden MAPI-Aufrufe.**

![Fehlermeldung für die meisten Cross-Bitness MAPI-Aufrufe] (media/738905fb-57ae-4af7-b54b-a1676c80d3c3.JPG "Fehlermeldung für die meisten Cross-Bitness MAPI-Aufrufe")
  
Ein Funktionsaufruf zwischen allen Simple MAPI- und MAPI-Elementen, **MAPISendMail**, wird jedoch erfolgreich in einem WOW64-Szenario (Windows-32-bit-on-Windows-64-bit) oder WOW32-Szenario (Windows-64-bit-on-Windows-32-bit) erfolgreich ausgef�hrt und gibt nicht die oben dargestellte Warnmeldung zur�ck. Dieses WOW64-Szenario gilt nur f�r Windows�7. 

In Abbildung�2 wird ein WOW64-Szenario dargestellt, in dem eine 32-Bit-MAPI-Anwendung **MAPISendMail** auf einem Computer mit der 64-Bit-Version von Windows�7 aufruft. In diesem Szenario f�hrt die MAPI-Bibliothek einen COM-Aufruf durch, um eine 64-Bit-Fixmapi-Anwendung zu starten. Die Fixmapi-Anwendung verweist implizit auf die MAPI-Bibliothek, die den Funktionsaufruf an den Windows-MAPI-Stub weiterleitet, wodurch wiederum der Aufruf an den Outlook-MAPI-Stub weitergeleitet wird und so der **MAPISendMail**Funktionsaufruf erfolgreich ausgef�hrt werden kann. 
  
**Abbildung�2. Verarbeiten von MAPISendMail in einem WOW64-Szenario.**

![Verarbeiten von MAPISendMail in einem WOW64-Szenario] (media/346ba974-4844-4b64-9dd1-d0f829ab99b3.gif "Verarbeiten von MAPISendMail in einem WOW64-Szenario")
  
## <a name="see-also"></a>Siehe auch

- [Link zu MAPI-Funktionen](how-to-link-to-mapi-functions.md)

