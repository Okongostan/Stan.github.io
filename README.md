
// NOTE - github rate limits to 10 requests per minute
// returns map[filepath][list-of-broken-links-in-file]
func SearchGithub(username string, repoName string, path string) error {
	url := fmt.Sprintf("https://api.github.com/repos/%s/%s/contents/%s", username, repoName, path)
	fmt.Printf("\n\n Sleeping, then searching: %s", url)
lkhnuiogoui
