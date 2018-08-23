---
title: Dateiformat von MapiSvc.inf
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b48eda17-83a8-4dc4-85c8-4ca827d13d25
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 726d424b6cf8d3141b36c3b61a38a6928277ec2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567174"
---
# <a name="file-format-of-mapisvcinf"></a>Dateiformat von MapiSvc.inf

**Betrifft**: Outlook 2013 | Outlook 2016 
  
Die Datei "MapiSvc.inf" fungiert als MAPI-Nachricht Dienstkonfigurationsinformationen zur Konfiguration der zentralen Datenbank. MapiSvc.inf enthält Informationen zu den einzelnen die Message-Dienste auf der Arbeitsstation, Informationen zu den Dienstanbieter, die für jeden Nachrichtendienst gehören, und Informationen zu MAPI-Subsystems installiert. MapiSvc.inf ist die primäre Informationsquelle für Profile. D. h., wenn ein neues Profil erstellt wird oder eine vorhandene geändert, relevanten Informationen für jeden Nachrichtendienst oder Dienstanbieter aus MapiSvc.inf kopiert wird. 
  
MapiSvc.inf ist in verknüpften hierarchische Abschnitte unterteilt:
  
1. Abschnitt mit Informationen, die für alle Profile gilt. In diesem Abschnitt besteht aus drei Teilen:
    
   - Bereitstellen von Links zu allen der nachfolgenden Nachricht Service Abschnitte Abschnitt **[Services]** . 
    
   - Mit Informationen zum Abschnitt **[Help File Mappings]** . HLP-Dateien, die von den Diensten für Nachricht bereitgestellt. 
    
   - [Default] Sie im Abschnitt **Dienste** Auflisten von Message-Dienste, die eine Standardinstallation bilden. 
    
2. Abschnitt mit Informationen, die für einzelne Message Dienste gilt. Einträge in den folgenden Abschnitten finden Sie Links zu nachfolgenden Service Provider Abschnitte.
    
3. Abschnitt mit Informationen, die auf einzelne-Dienstanbieter in einem Nachrichtendienst angewendet wird.
    
Die folgende Abbildung zeigt die Organisation der einer typischen Datei "MapiSvc.inf". Es gibt drei Message-Dienste: AB, MsgService und MS. Der Name der rechts vom Gleichheitszeichen auf für jeden Nachrichtendienst ist Anzeigename für den Dienst. Jede Messagingdiensts verfügt über einen eigenen Abschnitt an anderer Stelle in der Datei, die mit einem oder mehreren Service Provider Abschnitten verknüpft ist. Es ist ein Dienst Anbieterabschnitt für jede Dienstanbieter, die den Dienst gehört. Die AB und MS Message-Dienste sind für die einmalige Dienste, während drei-Dienstanbieter mit dem Dienst MsgService gehören.
  
**Organisation der Datei "MapiSvc.inf"**
  
![Organisation der Datei MapiSvc.inf] (media/amapi_30.gif "Organisation der Datei MapiSvc.inf")
  
MAPI bietet eine skeletal Version der Datei "MapiSvc.inf" mit den Einträgen für die MAPI-Subsystems. Jede Nachricht Service Implementierer fügt Einträge, die sowohl für ihren Dienst und der Dienstanbieter, die ihren Dienst angehören, geeignet sind. Einige der Einträge sind erforderlich, während andere optional sind. Beispielsweise erfordert MAPI an, dass Sie den Namen und Pfad der einzelnen-Dienstanbieter in Ihrer Messagingdiensts angeben. Sie können nicht ohne diese Informationen geladen werden.
  
Sie können entweder im Abschnitt erforderlichen und optionalen Informationen für den Nachrichtendienst und/oder die Service Provider Abschnitte hinzufügen. Hier können Sie die Informationen zur Beschreibung Ihrer Messagingdiensts einfügen, hängt von der Anzahl der Dienstanbieter im Dienst. Da diese Informationen auf jeder Dienstanbieter im Dienst angewendet wird, müssen Sie es für alle Anbieter vornehmen. Speichern Sie sie im Abschnitt Nachricht Dienst, der die bevorzugte Option oder in allen Abschnitten Service Provider. Speichern Sie Informationen, sobald vermeiden Sie unnötige Replikation und die Notwendigkeit, mehrere Kopien synchronisiert.
  
Speichern Sie alle Informationen für den Dienst Nachricht, wenn Ihre Messagingdiensts einen einzigen Anbieter-Dienst ist in den Abschnitt für den Dienstanbieter nicht im Abschnitt für den Dienst. Zugreifen auf den Bereich Service Provider ist schneller und direkter als den Zugriff auf den Bereich Message Service. 
  
Speichern Sie nur öffentliche Konfigurationsdaten in der Datei "MapiSvc.inf". Informationen, die private oder erfordert zusätzliche Schutz, beispielsweise Kennwörtern oder andere Anmeldeinformationen sollte nicht in der Datei aufgenommen werden. Stattdessen Wahl, entweder keine Informationen dieses Typs in allen Speichern oder als sicheren Eigenschaften im Benutzerprofil aufbewahren. Schützen von Eigenschaften haben integrierten Schutzfeatures wie beispielsweise Verschlüsselung.
  

