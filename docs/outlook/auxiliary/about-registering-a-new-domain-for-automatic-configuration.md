---
title: Informationen zum Registrieren einer neuen Domäne für die automatische Konfiguration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: a7ab8a50-dd30-4ba5-b6d8-e6d1f482e6f1
description: Outlook bietet eine Möglichkeit zum Angeben einer neuen Nachrichtendienst Domäne für die automatische Konfiguration und ermöglicht es dem Nachrichtendienst Anbieter, das Konto zu konfigurieren.
ms.openlocfilehash: bf06ff8d145ed6173e3545f784f8b5b7b5f433be
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316968"
---
# <a name="about-registering-a-new-domain-for-automatic-configuration"></a>Informationen zum Registrieren einer neuen Domäne für die automatische Konfiguration

Outlook bietet eine Möglichkeit zum Angeben einer neuen Nachrichtendienst Domäne für die automatische Konfiguration und ermöglicht es dem Nachrichtendienst Anbieter, das Konto zu konfigurieren.
  
Beim Entwerfen eines Nachrichtendienst Anbieters können Sie den folgenden Schlüssel in der Windows-Registrierung verwenden, um eine neue Domäne anzugeben, die automatisch vom entsprechenden Nachrichtendienst Anbieter konfiguriert werden soll: 
  
`HKLM\Software\Microsoft\Office\Outlook\AutoConfigDomains\<domain name>\`
  
Im Schlüssel `<domain name>` ist die Domäne für die automatische Konfiguration. Dieser Domänenname unterstützt nur \* am Anfang einen Platzhalter. In der folgenden Tabelle sind die von diesem Schlüssel unterstützten Werte aufgeführt. 
  
| Wert | Typ | Beschreibung |
|:-----|:-----|:-----|
|Anzeigename  <br/> |REG_SZ  <br/> |Der Domänenname, der dem Benutzer während der automatischen Konfiguration angezeigt wird.  <br/> |
|Dienst Name  <br/> |REG_SZ  <br/> |Der in MAPISVC. inf registrierte Nachrichtendienst, der diese Domäne unterstützt.  <br/> |
|Installationsspeicherort  <br/> |REG_SZ  <br/> |Die URL des Speicherorts, an dem der Nachrichtendienst Anbieter installiert werden soll, falls er noch nicht installiert ist.  <br/> |
|MindestVersion  <br/> |REG_DWORD  <br/> |Die mindestens erforderliche Version der DLL des Nachrichtendienst Anbieters. Dieser Wert ist optional.  <br/> |
   
Wenn Outlook die automatische Konfiguration für ein e-Mail-Konto startet, prüft es die Windows-Registrierung nach der Registrierung der Domäne, die von der e-Mail-Adresse angegeben wird. Wenn die Domäne bereits in der Windows-Registrierung angegeben ist, überprüft Outlook, ob der Nachrichtendienst in MAPISVC. inf registriert ist. Outlook kann nicht mit der automatischen Konfiguration der Domäne fortfahren, es sei denn, es wurde in der Windows-Registrierung angegeben.
  
Wenn der angegebene Nachrichtendienst derzeit nicht in MAPISVC. inf registriert ist oder wenn der Nachrichtendienst Anbieter installiert ist, aber die DLL eine Version vor dem angegebenen Minimum hat, verwendet Outlook den angegebenen Anzeigenamen und fordert den Benutzer auf, die Anbieter. Wenn der Benutzer akzeptiert, leitet Outlook den Benutzer an den angegebenen Installationsspeicherort um, sodass der Benutzer den Anbieter installieren kann. Durch die Installation des Anbieters wird der Nachrichtendienst in MAPISVC. inf registriert.
  
Wenn der Nachrichtendienst derzeit in MAPISVC. inf registriert ist und die Dienstanbieter. dll eine geeignete Version ist, erstellt Outlook den Nachrichtendienst mithilfe von [IMsgServiceAdmin:: CreateMsgService](https://msdn.microsoft.com/library/0135f049-0311-45e5-9685-78597d599a4e%28Office.15%29.aspx)und konfiguriert ihn dann mithilfe von [ IMsgServiceAdmin:: ConfigureMsgService](https://msdn.microsoft.com/library/a08f5905-2585-49ca-abb7-a77f2736f604%28Office.15%29.aspx). Die automatische Outlook-Konfiguration verwendet die folgenden drei Eigenschaften, damit der Anbieter das Konto einrichten kann: [pidtagautoconfigurationusername (](https://msdn.microsoft.com/library/05dfa0e2-4ab1-4f57-9009-6a815aca87bd%28Office.15%29.aspx), [pidtagautoconfigurationuseremail (](https://msdn.microsoft.com/library/845140c8-5454-4b47-acec-ab5aff00b768%28Office.15%29.aspx)und [pidtagautoconfigurationuserpassword ( ](https://msdn.microsoft.com/library/d33e7c45-55d8-4dc1-ade9-605542d87e61%28Office.15%29.aspx).
  
## <a name="see-also"></a>Siehe auch

- [Datei Format von MapiSvc. inf](https://msdn.microsoft.com/library/b48eda17-83a8-4dc4-85c8-4ca827d13d25%28Office.15%29.aspx)

