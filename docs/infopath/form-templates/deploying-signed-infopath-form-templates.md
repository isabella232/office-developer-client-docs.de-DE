---
title: Bereitstellen signierter InfoPath-Formularvorlagen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8345a4bc-ad7b-d0b0-7615-f77ade35006d
description: Bevor Sie dieses Thema lesen, finden Sie unter TheSigned Formular Templatessection in zusätzliche Sicherheitskonzepte für InfoPath-Formular für einen Überblick über die Sicherheit signierter Formularvorlagen. Informationen und Diskussionen im Thema Sicherheitsstufen, Bereitstellung per E-Mail und Remoteformularvorlagen sind auch relevant.
ms.openlocfilehash: de64cb0efdbbdd11a301d89ced03e63454849adb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790721"
---
# <a name="deploying-signed-infopath-form-templates"></a>Bereitstellen signierter InfoPath-Formularvorlagen

Bevor Sie dieses Thema lesen, finden Sie unter "Signierter Formularvorlagen" in der im Abschnitt [Zusätzliche Sicherheitskonzepte für InfoPath-Formular](additional-infopath-form-security-concepts.md) einen Überblick über die Sicherheit signierter Formularvorlagen. Informationen und Diskussionen im Thema [Sicherheitsstufen, Bereitstellung, per E-Mail und Remoteformularvorlagen](security-levels-email-deployment-and-remote-form-templates.md) sind auch relevant. 
  
## <a name="digitally-signing-a-form-template"></a>Digitales Signieren einer Formularvorlage

Wenn Sie eine Formularvorlage digital signieren, können Sie die Sicherheitsstufe für die Formularvorlage voll vertrauenswürdig festlegen, was bedeutet, dass das Formular Dateien und Einstellungen auf dem Computer des Benutzers oder in einer anderen Domäne zugreifen kann. (Darüber hinaus digitales Signieren einer Formularvorlage nicht verhindert mit anderen Sicherheitsstufen, falls gewünscht. Sie legen die Sicherheitsstufe einer signierten Formularvorlage auf die Sicherheitsstufe Domäne oder eingeschränkt erfordert.) Darüber hinaus können Sie signierten Formularvorlage für Benutzer bereitzustellen, die ein e-Mail-Programm verwenden und dann später automatisch aktualisieren signierten Formularvorlage durch die aktualisierte Version als Anlage einer e-Mail-Nachricht an die Benutzer senden, gehen Sie folgendermaßen vor:
  
### <a name="to-digitally-sign-a-form-template"></a>So können Sie eine Formularvorlage digital signieren

1. Klicken Sie im InfoPath-Designer auf der Registerkarte **Datei** , und klicken Sie dann auf der Registerkarte **Info** auf **Formularoptionen** . 
    
2. Klicken Sie im Dialogfeld **Formularoptionen** auf die Kategorie **Sicherheit und Vertrauensstellung** . 
    
3. Aktivieren Sie das Kontrollkästchen **Diese Formularvorlage signieren** , klicken Sie unter **Signatur der Formularvorlage**. 
    
4. Klicken Sie auf **Zertifikat auswählen**.
    
5. Klicken Sie im Dialogfeld **Zertifikat auswählen** auf das Zertifikat, das Sie verwenden, um das Formular digital signieren möchten. 
    
> [!NOTE]
> Die Schaltfläche **Zertifikat erstellen** , klicken Sie im Dialogfeld **Formularoptionen** kann zum Generieren eines Testzertifikats zum Signieren einer Formularvorlage verwendet werden. Das Testzertifikat sollte zum Signieren von Formularvorlagen nur zu Testzwecken verwendet werden. Testzertifikate sollte nicht verwendet werden, zum Signieren von Formularvorlagen, die öffentlich verteilt werden. Da die Zertifikate nicht von einer Zertifizierungsstelle ausgestellt werden, deren Stammzertifikat möglicherweise bereits auf dem Computer eines Benutzers als vertrauenswürdig wird, überprüft das Testzertifikat nicht richtig auf dem Computer des Benutzers. Wenn Sie eine mit einem Testzertifikat signierte Formularvorlage bereitstellen, werden die Formularvorlage Benutzer wahrscheinlich nicht öffnen können. 
  
## <a name="establishing-a-trusted-root-certificate-and-publisher"></a>Einrichten eines vertrauenswürdigen Stammzertifikats und eines vertrauenswürdigen Herausgebers

  Das vertrauenswürdige Stammzertifikat des Zertifikats, mit dem die Formularvorlage signiert wird, muss im Speicher für vertrauenswürdige Stammzertifikate auf dem Clientcomputer vorhanden sein. Andernfalls kann der Herausgeber der Formularvorlage nicht überprüft werden, und Benutzer Ihrer Formularvorlage haben nicht die Möglichkeit, dem Herausgeber zu vertrauen. Falls sich das vertrauenswürdige Stammzertifikat im Speicher für vertrauenswürdige Stammzertifikate befindet, aber der Herausgeber nicht in der Liste vertrauenswürdiger Herausgeber vorhanden ist, werden die Benutzer aufgefordert bzw. haben die Möglichkeit, dem Herausgeber der Formularvorlage zu vertrauen. 
  
> [!NOTE]
> Wenn eine signierte Formularvorlage die Domänensicherheitsstufe oder die eingeschränkte Sicherheitsstufe erfordert, überprüft InfoPath mithilfe der Signatur, ob die Formularvorlage nach dem Signieren manipuliert wurde. Außerdem bestimmt InfoPath mithilfe der Signatur, ob die Formularvorlage automatisch aktualisiert werden kann. 
  
## <a name="deploying-signed-form-templates-with-full-trust-access"></a>Bereitstellen signierter Formularvorlagen mit der Sicherheitsstufe "Voll vertrauenswürdig"

Das primäre Szenario für Bereitstellen signierter Formularvorlagen ist so aktivieren Sie Domäne-ähnliche Funktionalität wie automatische Updates, voll vertrauenswürdige Formulare. Eine signierte Formularvorlage, die voll vertrauenswürdigen Zugriff anfordern hat den gleichen Zugriff auf Systemressourcen wie ein *voll vertrauenswürdiges Formular* . Eine ausführliche Erläuterung der Funktionsweise voll vertrauenswürdiger Formulare und zum Erstellen und Bereitstellen finden Sie unter [Grundlegendes zu voll vertrauenswürdigen Formularen](understanding-fully-trusted-forms.md).
  
In Abhängigkeit von der EDV-Umgebung Ihrer Organisation ziehen Sie jedoch möglicherweise die Verwendung signierter Formularvorlagen oder voll vertrauenswürdiger Formulare vor. Beispielsweise bietet die Verwendung einer signierten Formularvorlage, die die Sicherheitsstufe Voll vertrauenswürdig erfordert, anstelle eines registrierten, voll vertrauenswürdigen Formulars die folgenden Vorteile:
  
- Im Gegensatz zu einer unsignierten, voll vertrauenswürdigen Formularvorlage ist keine Registrierung erforderlich.
    
- Die automatische Aktualisierung der Formularvorlage ist möglich.
    
Da eine signierte Formularvorlage, die die Sicherheitsstufe Voll vertrauenswürdig erfordert, keine Registrierung erfordert, müssen Sie diese nicht mit einem Installer-Paket oder einer Skriptdatei bereitstellen. Dadurch wird die Bereitstellung einer voll vertrauenswürdigen Formularvorlage erheblich vereinfacht.
  
Beim Aktualisieren der signierten Formularvorlage, die die Sicherheitsstufe Voll vertrauenswürdig erfordert, können Sie einfach die aktualisierte Vorlage an den Benutzer senden oder diese in einem freigegebenen Speicherort aktualisieren. Wenn der Benutzer die aktualisierte Vorlage öffnet, wird der Benutzer nicht aufgefordert, und die ältere Kopie auf dem Computer des Benutzers wird automatisch mit der aktualisierten Version überschrieben. Falls Sie die Vorlage in einem freigegebenen Speicherort aktualisiert haben, kann der Benutzer die aktualisierte Kopie ohne Bestätigung verwenden.
  
Falls Sie ein unsigniertes, voll vertrauenswürdiges Formular aktualisieren möchten, müssen Sie das Formular erneut packen und registrieren. Darüber hinaus kann eine vorhandene und installierte voll vertrauenswürdige Formularvorlage nur für den Pfad des lokalen Computers, nicht aber für einen Netzwerkpfad verwendet werden, da für den Registrierungsvorgang ein lokaler Computerpfad nicht in einen Netzwerkpfad geändert werden kann. Da allerdings ein Zertifikat zum Signieren einer Formularvorlage erforderlich ist, sollten Sie eventuell voll vertrauenswürdige, registrierte Formularvorlagen bereitstellen, wenn Sie kein Zertifikat erwerben möchten.
  
## <a name="deploying-signed-form-templates-with-domain-or-restricted-access"></a>Bereitstellen signierter Formularvorlagen mit der Domänensicherheitsstufe oder der eingeschränkten Sicherheitsstufe 

Eine signierte Formularvorlage, die Sicherheitsstufe Domäne oder eingeschränkt wurde, hat auch den Vorteil die automatische Updatefunktion. Beispielsweise könnten Sie eine signierte Formularvorlage in einer Dokumentbibliothek auf einem Server, auf der Microsoft SharePoint Foundation ausgeführt wird oder auf einem Server mit einer Domänensicherheitsstufe veröffentlichen. Wenn Sie die Formularvorlage im freigegebenen Speicherort aktualisieren, erhalten Benutzer automatisch die aktualisierte Kopie.
  

