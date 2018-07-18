---
title: Informationen zum Registrieren einer neuen Domäne für die automatische Konfiguration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a7ab8a50-dd30-4ba5-b6d8-e6d1f482e6f1
description: Outlook bietet eine Möglichkeit zum Angeben einer neuen Nachricht Service-Domäne für die automatische Konfiguration und ermöglichen die Nachricht-Dienstanbieters für das Dienstkonto konfiguriert.
ms.openlocfilehash: c1daea81fe18e5d1088a233a3fcdff076419d6bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790924"
---
# <a name="about-registering-a-new-domain-for-automatic-configuration"></a>Informationen zum Registrieren einer neuen Domäne für die automatische Konfiguration

Outlook bietet eine Möglichkeit zum Angeben einer neuen Nachricht Service-Domäne für die automatische Konfiguration und ermöglichen die Nachricht-Dienstanbieters für das Dienstkonto konfiguriert.
  
Beim Entwerfen eines Nachricht-Dienstanbieters können den folgenden Schlüssel in der Windows-Registrierung Sie eine neue Domäne automatisch konfiguriert werden, durch die entsprechende Nachricht-Dienstanbieter angeben: 
  
`HKLM\Software\Microsoft\Office\Outlook\AutoConfigDomains\<domain name>\`
  
In den Schlüssel `<domain name>` ist die Domäne für die automatische Konfiguration. Diesen Domänennamen ein Platzhalterzeichen unterstützt \* am Anfang nur. In der folgenden Tabelle sind die Werte dieser Schlüssel unterstützt. 
  
| Value | Typ | Beschreibung |
|:-----|:-----|:-----|
|Anzeigename  <br/> |REG_SZ  <br/> |Der Domänenname, der während der automatischen Konfiguration für den Benutzer angezeigt wird.  <br/> |
|Dienstname  <br/> |REG_SZ  <br/> |Der Nachrichtendienst registriert in mapisvc.inf, die von dieser Domäne unterstützt.  <br/> |
|Installationsspeicherort  <br/> |REG_SZ  <br/> |Die URL des Speicherorts den Nachricht-Dienstanbieter zu installieren, wenn es nicht bereits installiert ist.  <br/> |
|Mindestversion  <br/> |REG_DWORD  <br/> |Die minimale Version der DLL-Datei des Dienstanbieters Nachricht, die erforderlich ist. Dieser Wert ist optional.  <br/> |
   
Wenn Outlook die automatische Konfiguration für ein e-Mail-Konto beginnt, überprüft die Windows-Registrierung für die Registrierung von der Domäne, die durch die e-Mail-Adresse angegeben. Wenn die Domäne bereits in der Windows-Registrierung angegeben wird, überprüft Outlook an, ob der Nachrichtendienst in Mapisvc.inf registriert ist. Outlook kann nicht mit der automatischen Konfiguration der Domäne fortgesetzt, es sei denn, es in der Windows-Registrierung angegeben wurde.
  
Wenn Sie der angegebenen Dienst ist derzeit nicht in Mapisvc.inf, registriert oder der Nachricht-Dienstanbieter installiert ist, aber die DLL-Datei verfügt über eine Version vor dem angegebenen Mindestwert, Outlook verwendet den angegebenen Anzeigenamen und fordert den Benutzer zum Installieren der Anbieter. Wenn der Benutzer annimmt, leitet Outlook den Benutzer zum angegebenen Installationsspeicherort, damit der Benutzer den Anbieter installieren kann. Installieren den Anbieter registriert den Dienst in Mapisvc.inf.
  
Wenn der Nachrichtendienst ist derzeit in Mapisvc.inf registriert, und die Service Provider DLL-Datei eine geeignete Version ist, Outlook Message-Dienst mithilfe von [IMsgServiceAdmin:: CreateMsgService](http://msdn.microsoft.com/library/0135f049-0311-45e5-9685-78597d599a4e%28Office.15%29.aspx)erstellt und konfiguriert es anschließend mithilfe von [ IMsgServiceAdmin::ConfigureMsgService](http://msdn.microsoft.com/library/a08f5905-2585-49ca-abb7-a77f2736f604%28Office.15%29.aspx). Automatische Konfiguration von Outlook verwendet die folgenden drei Eigenschaften zum Zulassen des Dienstanbieters für das Konto eingerichtet: [PidTagAutoConfigurationUserName](http://msdn.microsoft.com/library/05dfa0e2-4ab1-4f57-9009-6a815aca87bd%28Office.15%29.aspx), [PidTagAutoConfigurationUserEmail](http://msdn.microsoft.com/library/845140c8-5454-4b47-acec-ab5aff00b768%28Office.15%29.aspx)und [PidTagAutoConfigurationUserPassword ](http://msdn.microsoft.com/library/d33e7c45-55d8-4dc1-ade9-605542d87e61%28Office.15%29.aspx).
  
## <a name="see-also"></a>Siehe auch

- [Dateiformat von MapiSvc.inf](http://msdn.microsoft.com/library/b48eda17-83a8-4dc4-85c8-4ca827d13d25%28Office.15%29.aspx)

