# Spring-Boot-Notions


Spring Boot est une extension du framework Spring qui simplifie le développement d'applications Java en fournissant des configurations par défaut. Il utilise un grand nombre d'annotations pour configurer et gérer divers aspects de l'application. Voici une liste des annotations les plus courantes en Spring Boot, avec leurs rôles et leurs utilisations :

### 1. **Annotations de Configuration**

- **`@SpringBootApplication`** : Combine trois annotations en une (`@Configuration`, `@EnableAutoConfiguration`, `@ComponentScan`). Utilisée sur la classe principale pour indiquer qu'il s'agit d'une application Spring Boot.

- **`@Configuration`** : Indique que la classe contient des configurations Spring. Elle remplace généralement les fichiers de configuration XML.

- **`@ComponentScan`** : Configure le package à scanner pour les composants Spring (comme `@Component`, `@Service`, `@Repository`, etc.). Par défaut, elle scanne le package dans lequel la classe annotée est située.

- **`@EnableAutoConfiguration`** : Indique à Spring Boot de configurer automatiquement les beans en fonction des dépendances présentes sur le classpath.

- **`@PropertySource`** : Spécifie un ou plusieurs fichiers de propriétés à charger dans l'environnement Spring.

### 2. **Annotations de Composants**

- **`@Component`** : Indique qu'une classe est un composant Spring, ce qui signifie qu'elle sera détectée et gérée par le conteneur Spring.

- **`@Service`** : Spécialisation de `@Component` pour indiquer que la classe est un service (contenant la logique métier).

- **`@Repository`** : Spécialisation de `@Component` utilisée pour indiquer que la classe est un dépôt (généralement, elle encapsule l'accès à une source de données).

- **`@Controller`** : Spécialisation de `@Component` pour indiquer qu'une classe est un contrôleur MVC (Model-View-Controller).

- **`@RestController`** : Combinaison de `@Controller` et `@ResponseBody`. Indique que les méthodes de la classe retourneront directement des données au format JSON ou XML plutôt qu'une vue.

### 3. **Annotations pour la Gestion des Requêtes Web**

- **`@RequestMapping`** : Mappage des requêtes HTTP à des méthodes de contrôleur. Peut être utilisé au niveau de la classe ou de la méthode.

- **`@GetMapping`, `@PostMapping`, `@PutMapping`, `@DeleteMapping`, `@PatchMapping`** : Spécialisations de `@RequestMapping` pour les différentes méthodes HTTP (GET, POST, PUT, DELETE, PATCH).

- **`@PathVariable`** : Indique que le paramètre de méthode doit être lié à une variable de chemin d'URI.

- **`@RequestParam`** : Indique que le paramètre de méthode doit être lié à un paramètre de requête HTTP.

- **`@RequestBody`** : Indique que le paramètre de méthode doit être lié au corps d'une requête HTTP.

- **`@ResponseBody`** : Indique que le retour d'une méthode sera sérialisé en JSON ou XML et écrit directement dans le corps de la réponse HTTP.

### 4. **Annotations pour la Gestion des Transactions**

- **`@Transactional`** : Indique qu'une méthode ou une classe entière doit être exécutée dans une transaction. Si une exception non contrôlée survient, la transaction sera annulée.

### 5. **Annotations pour la Sécurité**

- **`@Secured`** : Spécifie les rôles autorisés à exécuter une méthode.

- **`@PreAuthorize`** : Permet de spécifier des conditions d'accès aux méthodes via des expressions SpEL (Spring Expression Language).

- **`@RolesAllowed`** : Similaire à `@Secured`, spécifie les rôles autorisés.

- **`@EnableWebSecurity`** : Active la configuration de la sécurité web dans une application Spring Boot.

### 6. **Annotations pour la Validation**

- **`@Valid`** : Indique que l'objet de la méthode doit être validé par le framework de validation Bean Validation (JSR 303/JSR 380).

- **`@NotNull`, `@NotEmpty`, `@Size`, `@Min`, `@Max`, etc.** : Annotations de validation utilisées pour valider les champs d'un bean en fonction de certaines contraintes.

### 7. **Annotations pour les Tests**

- **`@SpringBootTest`** : Indique qu'une classe de test doit charger le contexte de l'application Spring. Utilisé pour les tests d'intégration.

- **`@MockBean`** : Remplace un bean dans le contexte de l'application par un mock, utile pour isoler les tests unitaires.

- **`@WebMvcTest`** : Charge uniquement les composants Spring MVC pour les tests, comme les contrôleurs.

- **`@DataJpaTest`** : Charge uniquement les composants JPA pour les tests, idéal pour tester les dépôts.

### 8. **Annotations pour la Gestion des Propriétés**

- **`@Value`** : Injecte la valeur d'une propriété (par exemple, d'un fichier `application.properties`) dans un champ ou un paramètre de méthode.

- **`@ConfigurationProperties`** : Lie les propriétés d'un fichier de configuration à un objet Java.

### 9. **Annotations pour la Gestion des tâches**

- **`@Scheduled`** : Indique qu'une méthode doit être exécutée de manière planifiée.

- **`@EnableScheduling`** : Active le support de la planification des tâches avec `@Scheduled`.

### 10. **Annotations de Stéréotypes**

- **`@Aspect`** : Indique qu'une classe est un aspect, une partie du modèle de programmation orientée aspect.

- **`@EnableAspectJAutoProxy`** : Active le support de la programmation orientée aspect avec AspectJ.

Ces annotations simplifient la configuration, la gestion des composants, la sécurité, la validation, les transactions, et bien plus encore, en offrant une approche déclarative pour développer des applications robustes avec Spring Boot.
