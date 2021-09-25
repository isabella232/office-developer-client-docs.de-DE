---
title: Informationen zum Registrieren einer neuen Domäne für die automatische Konfiguration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: a7ab8a50-dd30-4ba5-b6d8-e6d1f482e6f1
description: Outlook bietet eine Möglichkeit, eine neue Nachrichtendienstdomäne für die automatische Konfiguration anzugeben und dem Nachrichtendienstanbieter das Konfigurieren des Kontos zu ermöglichen.
ms.openlocfilehash: c038bf3461a3452b692687b1a2f6f541c2e45092
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572242"
---
# <a name="about-registering-a-new-domain-for-automatic-configuration"></a>Informationen zum Registrieren einer neuen Domäne für die automatische Konfiguration

Outlook bietet eine Möglichkeit, eine neue Nachrichtendienstdomäne für die automatische Konfiguration anzugeben und dem Nachrichtendienstanbieter das Konfigurieren des Kontos zu ermöglichen.
  
Beim Entwerfen eines Nachrichtendienstanbieters können Sie den folgenden Schlüssel in der Windows Registrierung verwenden, um eine neue Domäne anzugeben, die automatisch vom entsprechenden Nachrichtendienstanbieter konfiguriert werden soll: 
  
`HKLM\Software\Microsoft\Office\Outlook\AutoConfigDomains\<domain name>\`
  
Im Schlüssel `<domain name>` befindet sich die Domäne für die automatische Konfiguration. Dieser Domänenname unterstützt nur am Anfang einen \* Platzhalter. In der folgenden Tabelle sind die Von diesem Schlüssel unterstützten Werte aufgeführt. 
  
| Wert | Typ | Beschreibung |
|:-----|:-----|:-----|
|Anzeigename  <br/> |REG_SZ  <br/> |Der Domänenname, der dem Benutzer während der automatischen Konfiguration angezeigt wird.  <br/> |
|Dienstname  <br/> |REG_SZ  <br/> |Der in mapisvc.inf registrierte Nachrichtendienst, der diese Domäne unterstützt.  <br/> |
|Installationsspeicherort  <br/> |REG_SZ  <br/> |Die URL des Speicherorts, an dem der Nachrichtendienstanbieter installiert werden soll, falls er noch nicht installiert ist.  <br/> |
|Mindestversion  <br/> |REG_DWORD  <br/> |Die mindest erforderliche Version des .dll des Nachrichtendienstanbieters. Dieser Wert ist optional.  <br/> |
   
Wenn Outlook die automatische Konfiguration für ein E-Mail-Konto beginnt, überprüft es die Windows Registrierung auf die Registrierung der durch die E-Mail-Adresse angegebenen Domäne. Wenn die Domäne bereits in der Windows-Registrierung angegeben ist, überprüft Outlook, ob der Nachrichtendienst in Mapisvc.inf registriert ist. Outlook kann nicht mit der automatischen Konfiguration der Domäne fortfahren, es sei denn, sie wurde in der Windows Registrierung angegeben.
  
Wenn der angegebene Nachrichtendienst derzeit nicht in Mapisvc.inf registriert ist oder der Nachrichtendienstanbieter installiert ist, der .dll jedoch eine version vor dem angegebenen Minimum hat, verwendet Outlook den angegebenen Anzeigenamen und fordert den Benutzer auf, den Anbieter zu installieren. Wenn der Benutzer dies zulässt, leitet Outlook den Benutzer an den angegebenen Installationsspeicherort weiter, damit der Benutzer den Anbieter installieren kann. Durch die Installation des Anbieters wird der Nachrichtendienst in Mapisvc.inf registriert.
  
Wenn der Nachrichtendienst derzeit in Mapisvc.inf registriert ist und der Dienstanbieter .dll eine geeignete Version ist, erstellt Outlook den Nachrichtendienst mithilfe von [IMsgServiceAdmin::CreateMsgService](https://msdn.microsoft.com/library/0135f049-0311-45e5-9685-78597d599a4e%28Office.15%29.aspx)und konfiguriert ihn dann mithilfe von [IMsgServiceAdmin::ConfigureMsgService.](https://msdn.microsoft.com/library/a08f5905-2585-49ca-abb7-a77f2736f604%28Office.15%29.aspx) Outlook automatische Konfiguration verwendet die folgenden drei Eigenschaften, damit der Anbieter das Konto einrichten kann: [PidTagAutoConfigurationUserName](https://msdn.microsoft.com/library/05dfa0e2-4ab1-4f57-9009-6a815aca87bd%28Office.15%29.aspx), [PidTagAutoConfigurationUserEmail](https://msdn.microsoft.com/library/845140c8-5454-4b47-acec-ab5aff00b768%28Office.15%29.aspx)und [PidTagAutoConfigurationUserPassword](https://msdn.microsoft.com/library/d33e7c45-55d8-4dc1-ade9-605542d87e61%28Office.15%29.aspx).
  
## <a name="see-also"></a>Siehe auch

- [Dateiformat von MapiSvc.inf](https://msdn.microsoft.com/library/b48eda17-83a8-4dc4-85c8-4ca827d13d25%28Office.15%29.aspx)

