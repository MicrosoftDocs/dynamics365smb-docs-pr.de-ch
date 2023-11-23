---
title: Copilot- und KI-Funktionen konfigurieren
description: 'In diesem Artikel wird erläutert, wie Sie Copilot in einer Umgebung aktivieren.'
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: how-to
ms.date: 10/29/2023
ms.custom: bap-template
ms.search.form: 7775
---

# <a name="configure-copilot-and-ai-capabilities"></a>Copilot- und KI-Funktionen konfigurieren

<!--[!INCLUDE[ai-preview](includes/ai-preview.md)]-->

<!--This article explains how you can control the ability to create AI-powered item marketing text with Copilot for your organization. This task is done by an admin. There are two requirements that you must fulfill to make the feature available to users:-->

In diesem Artikel wird erläutert, wie Sie den Benutzerzugriff auf Copilot und andere KI-Funktionen in Business Central steuern. Diese Aufgabe wird von Administrierenden erledigt. Abhängig von dem Feature gibt es drei Stufen der Zugriffskontrolle auf Copolit- und KI-Funktionen:

- Die Zustimmung zu den Bedingungen von Azure OpenAI [Vorschauversion](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) und zum [Datenschutz](https://go.microsoft.com/fwlink/?LinkId=521839).

   Diese Zustimmung ist erforderlich, damit alle Copilot- oder KI-Funktionen für Benutzende funktionieren. Die Zustimmung gilt global für alle Benutzenden und alle Copilot- und AI-Features. [Weitere Informationen](#consent-to-preview-and-privacy-terms)

- Datenverschiebung über geografische Regionen hinweg erlauben

  Diese Aufgabe ist nur erforderlich, wenn sich Ihre Business Central-Umgebung in einer anderen Region befindet als der Azure OpenAI Dienst, den sie verwendet. [Weitere Informationen](#allow-data-movement-across-geographies)

- Aktivieren Sie das spezifische Feature, wenn es noch von der **Funktionsverwaltung** gesteuert wird.

  Im 2. Veröffentlichungszyklus 2023 sind sowohl die Marketingtextvorschläge als auch die Features zur Unterstützung bei der Bankkontoabstimmung unter **Funktionsverwaltung** enthalten. Allerdings sind Marketingtextvorschläge standardmässig aktiviert. [Weitere Informationen](#enable-feature-in-feature-management)

- Aktivieren Sie das Feature auf der Seite **Copilot- und KI-Funktionen**. [Weitere Informationen](#activate-features)

Wenn eine dieser Anforderungen nicht erfüllt ist, steht das Feature nicht zur Verfügung.

## <a name="prerequisites"></a>Voraussetzungen

- Sie verwenden Business Central online, Version 23.1 oder höher. <!--[preview version](ai-preview-getstarted.md) of Business Central that's enabled for Copilot.-->
- Sie verfügen über Administrator- oder Superuserberechtigungen in Business Central.  <!--For more information, go to [Configure AI-powered item marketing text with Copilot](enable-ai.md).-->

## <a name="allow-data-movement-across-geographies"></a>Zustimmung zur Vorschauversion und den Datenschutzbestimmungen

Stimmen Sie für Ihre Organisation den Nutzungsbedingungen der [Vorschauversion](https://dynamics.microsoft.com/legaldocs/supp-dynamics365-preview/) und den [Microsoft-Datenschutzbestimmungen](https://go.microsoft.com/fwlink/?LinkId=521839) zu. Im Gegensatz zu Datenschutzhinweisen für andere Features und Dienste können nur Administrierende der Nutzung von Azure OpenAI zustimmen und tun dies im Namen der Organisation. Benutzende können nicht selbst entscheiden.   

1. Suchen Sie in Business Central nach der Seite **Status der Datenschutzhinweise** und öffnen Sie sie.
2. Wählen Sie in der Spalte **Integrationsname** **Azure OpenAI** aus und lesen Sie dann die Ihnen angezeigten Nutzungsbedingungen.
3. Aktivieren Sie in der Zeile **Azure OpenAI** das Kontrollkästchen **Für alle zustimmen**, um zuzustimmen, oder das Kontrollkästchen **Für alle ablehnen**, um abzulehnen.

## <a name="activate-features"></a>Aktivieren Sie das Feature in der Funktionsverwaltung

Die **Funktionsverwaltung** wird zum Aktivieren oder Deaktivieren von Features verwendet, die sich in der Vorschau befinden, z. B. der Bankkontoabstimmung, sowie einiger allgemein verfügbarer Features, z. B. Artikelmarketingvorschläge. [Weitere Informationen finden Sie unter Funktionsverwaltung](/dynamics365/business-central/dev-itpro/administration/feature-management).

1. Suchen und öffnen Sie in Business Central die Seite **Funktionsverwaltung**.
2. Um ein Feature zu aktivieren, legen Sie die Spalte **Aktiviert für** auf **Alle Benutzende** fest. Um ein Feature zu deaktivieren, legen Sie die Spalte **Aktiviert für** auf **Niemanden** fest. Verwenden Sie die folgende Tabelle, um den Umschalter zu bestimmen, der für die Copilot- und AO-Funktion gilt, die Sie aktivieren möchten:

   - **Funktionsvorschauversion: Bankkontoabstimmung mit Copilot** bezieht sich auf das Feature zur Unterstützung bei Bankkontoabstimmung.
   - **Funktionsvorschauversion: KI-gestützte Produktbeschreibungen mit Copilot erstellen** bezieht sich auf das Feature für Marketingtextvorschläge.

   Weitere Informationen zur Funktionsverwaltung im Allgemeinen finden Sie unter [Funktionsverwaltung](/dynamics365/business-central/dev-itpro/administration/feature-management).

## <a name="enable-feature-in-feature-management"></a>Datenverschiebung über geografische Regionen hinweg zulassen

Diese Aufgabe gilt nur, wenn der Umschalter **Datenverschiebung zulassen** oben auf der Seite **Copilot- und KI-Funktionen** erscheint. Der Umschalter **Datenverschiebung zulassen** gibt an, dass sich der Standort Ihrer Business Central-Umgebung – also die Region, in der Daten verarbeitet und gespeichert werden – nicht dieselbe ist wie die von Copilot verwendete Region für den Azure OpenAI-Dienst. Wenn Sie Copilot aktivieren möchten, müssen Sie die Datenverschiebung zwischen Regionen zulassen. Weitere Informationen zur Datenverschiebung finden Sie unter [Copilot-Datenverschiebung über geografische Regionen hinweg](ai-copilot-data-movement.md). 

Um die Datenverschiebung ausserhalb Ihrer geografischen Region zuzulassen, gehen Sie wie folgt vor:

1. Suchen Sie in Business Central nach der Seite **Copilot- und KI-Funktionen** und öffnen Sie sie.
1. Aktivieren Sie den Umschalter **Datenverschiebung zulassen**.

   ![![Alternativer Text](allow-data-movement.png)](allow-data-movement.png)

Sie können sich abmelden, indem Sie den Umschalter **Datenverschiebung zulassen** ausschalten. Sobald ein Azure OpenAI Dienst in der geografischen Region Ihrer Business Central-Umgebung verfügbar wird, wird Ihre Umgebung automatisch damit verbunden und der Umschalter ist nicht mehr verfügbar. 


<!--
| Australia, United Kingdom, United States | Within the respective geographical region |
| Europe, France, Germany, Norway, Switzerland  | Sweden or Switzerland |
| Asia Pacific, Brazil, Canada, India, Japan, Singapore, South Africa, South Korea, United Arab Emirates  | United States |-->



<!--Note

If your environment is hosted in North America, Copilot will use an Azure OpenAI endpoint in North America to process your data.
If your environment is hosted in Europe, Copilot will use an Azure OpenAI endpoint in Europe to process your data.
If your environment is hosted anywhere else, Copilot will use an Azure OpenAI endpoint outside of the region in which the environment is hosted.
To opt in 

Copilot and other AI capabilities use Azure OpenAI Service.  and are provided by default to only those customers with environments that have United States as their geography for data processing and storage. While the Azure OpenAI Service is available in multiple geographies including Australia, Canada, United States, France, Japan and UK, Copilot does not follow the same regional rollout schedule.

Meanwhile, customers with environments outside the United States can use Copilot AI features by opting in to share relevant data with the Azure OpenAI Service in United States or Switzerland.

The information in the following table outlines the Azure OpenAI service that's used by the Copilot services based on the geography of their Dynamics 365 environment when they opt-in to share data.-->
## <a name="granting-user-access"></a>Features aktivieren

Mit der Seite **Copilot- und KI-Funktionen** können Sie einzelne Features für alle Benutzenden aktivieren oder deaktivieren.

1. Suchen Sie in Business Central nach der Seite **Copilot- und KI-Funktionen** und öffnen Sie sie.

1. Die Seite listet alle verfügbaren Copilot- und KI-bezogenen Features und ihren aktuellen Status auf, der entweder aktiv oder inaktiv sein kann. Die Features sind in zwei Abschnitte unterteilt – ein Abschnitt für Features in der Vorschau und ein anderer für allgemein verfügbare Features. 

   [![Zeigt das Business Central-Rollencenter und die Checkliste für Copilot an](media/copilot-and-ai-capabilties-page.svg)](media/copilot-and-ai-capabilties-page.svg#lightbox)

   - Um ein Feature zu aktivieren, wählen Sie es in der Liste aus und wählen Sie dann im Menüband **Aktivieren** aus.
   - Um ein Feature zu deaktivieren, wählen Sie es in der Liste aus und wählen Sie dann im Menüband **Deaktivieren** aus. 


## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie die Features aktiviert und ihnen zugestimmt haben, können Sie sie ausprobieren. Gehen Sie zu:

- [Marketingtext zu Artikeln hinzufügen](item-marketing-text.md) 
- [Abstimmung mithilfe der Unterstützung bei Bankkontoabstimmung](bank-reconciliation-with-copilot.md) 

## <a name="see-also"></a>Siehe auch

[Überblick über Vorschläge für Marketingtexte](ai-overview.md)   
[Häufig gestellte Fragen zu Vorschlägen für Marketingtexte](faqs-marketing-text.md)  
